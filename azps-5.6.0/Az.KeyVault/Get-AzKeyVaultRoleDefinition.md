---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: b5d5da8c02081437f064fc1d2a6a29a5b772e8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001434"
---
# <span data-ttu-id="1ecce-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1ecce-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="1ecce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ecce-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecce-103">Lista definicji ról danego zarządzanego modułu HSM w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="1ecce-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="1ecce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1ecce-104">SYNTAX</span></span>

### <span data-ttu-id="1ecce-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1ecce-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ecce-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1ecce-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecce-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1ecce-107">DESCRIPTION</span></span>
<span data-ttu-id="1ecce-108">Lista definicji ról danego zarządzanego modułu HSM w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="1ecce-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="1ecce-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1ecce-109">EXAMPLES</span></span>

### <span data-ttu-id="1ecce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ecce-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="1ecce-111">W przykładzie wymieniono wszystkie role w zakresie "/keys".</span><span class="sxs-lookup"><span data-stu-id="1ecce-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="1ecce-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1ecce-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="1ecce-113">W tym przykładzie jest sprawdzana rola zarządzanej kopii zapasowej HSM i sprawdzane są jej uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="1ecce-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="1ecce-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ecce-114">PARAMETERS</span></span>

### <span data-ttu-id="1ecce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecce-115">-DefaultProfile</span></span>
<span data-ttu-id="1ecce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecce-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="1ecce-117">-HsmName</span></span>
<span data-ttu-id="1ecce-118">Nazwa hsm.</span><span class="sxs-lookup"><span data-stu-id="1ecce-118">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecce-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1ecce-119">-RoleDefinitionName</span></span>
<span data-ttu-id="1ecce-120">Nazwa definicji roli do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="1ecce-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecce-121">— Zakres</span><span class="sxs-lookup"><span data-stu-id="1ecce-121">-Scope</span></span>
<span data-ttu-id="1ecce-122">Zakres, do którego ma zastosowanie przypisanie roli lub definicja, np. '/' lub '/keys' lub '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="1ecce-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="1ecce-123">W przypadku pominięcia tej przeoczonej godziny należy użyć "/".</span><span class="sxs-lookup"><span data-stu-id="1ecce-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecce-124">CommonParameters</span></span>
<span data-ttu-id="1ecce-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ecce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecce-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ecce-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecce-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ecce-127">INPUTS</span></span>

### <span data-ttu-id="1ecce-128">Brak</span><span class="sxs-lookup"><span data-stu-id="1ecce-128">None</span></span>

## <span data-ttu-id="1ecce-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ecce-129">OUTPUTS</span></span>

### <span data-ttu-id="1ecce-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1ecce-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="1ecce-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1ecce-131">NOTES</span></span>

## <span data-ttu-id="1ecce-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ecce-132">RELATED LINKS</span></span>
