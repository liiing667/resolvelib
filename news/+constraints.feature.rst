Added a ``constraints`` argument to ``Resolver.resolve()``. Constraints are
(requirement, parent) pairs that only filter provider-returned candidates
(re-applied after every backtrack); they are never pinned and never appear in
``ResolutionImpossible.causes``. Failures caused by constraints raise the new
``ConstraintsConflicted`` exception, a subclass of ``ResolutionImpossible``.
