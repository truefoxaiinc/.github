# Docker deployment

Use reproducible multi-stage builds, a non-root runtime user, explicit health checks and minimal base images. Pin base-image versions, scan images, avoid embedding secrets and keep build-time and runtime configuration separate.

Document build, migration, startup, readiness, observability, backup and rollback procedures. Production deployment should use a managed secret store rather than committed environment files.
