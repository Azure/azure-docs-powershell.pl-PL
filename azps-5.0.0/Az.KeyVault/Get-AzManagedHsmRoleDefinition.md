---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
ms.openlocfilehash: 60ba6fbf57fa9e1ac9e25a913fb9755902b56ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224273"
---
# <span data-ttu-id="9e2ae-101">Get-AzManagedHsmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9e2ae-101">Get-AzManagedHsmRoleDefinition</span></span>

## <span data-ttu-id="9e2ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2ae-103">Wyświetlanie definicji ról określonego zarządzanego modułu HSM w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="9e2ae-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="9e2ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e2ae-104">SYNTAX</span></span>

### <span data-ttu-id="9e2ae-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9e2ae-105">Interactive (Default)</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e2ae-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9e2ae-106">ByName</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e2ae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e2ae-107">DESCRIPTION</span></span>
<span data-ttu-id="9e2ae-108">Wyświetlanie definicji ról określonego zarządzanego modułu HSM w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="9e2ae-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="9e2ae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e2ae-109">EXAMPLES</span></span>

### <span data-ttu-id="9e2ae-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e2ae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleDefinition -HsmName myHsm -Scope "/keys"

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

<span data-ttu-id="9e2ae-111">W przykładzie jest wyświetlana lista wszystkich ról w zakresie "/Keys".</span><span class="sxs-lookup"><span data-stu-id="9e2ae-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="9e2ae-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9e2ae-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzManagedHsmRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

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

<span data-ttu-id="9e2ae-113">W przykładzie jest pobierana rola "Zarządzana kopia zapasowa HSM" oraz zbadanie jej uprawnień.</span><span class="sxs-lookup"><span data-stu-id="9e2ae-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="9e2ae-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e2ae-114">PARAMETERS</span></span>

### <span data-ttu-id="9e2ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2ae-115">-DefaultProfile</span></span>
<span data-ttu-id="9e2ae-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e2ae-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="9e2ae-117">-HsmName</span></span>
<span data-ttu-id="9e2ae-118">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="9e2ae-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="9e2ae-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9e2ae-119">-RoleDefinitionName</span></span>
<span data-ttu-id="9e2ae-120">Nazwa definicji roli do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9e2ae-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="9e2ae-121">-Zakres</span><span class="sxs-lookup"><span data-stu-id="9e2ae-121">-Scope</span></span>
<span data-ttu-id="9e2ae-122">Zakres, na który dotyczy przypisanie roli lub definicja, na przykład "/" lub "/Keys" lub "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="9e2ae-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="9e2ae-123">w przypadku pominięcia użyto "/".</span><span class="sxs-lookup"><span data-stu-id="9e2ae-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="9e2ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2ae-124">CommonParameters</span></span>
<span data-ttu-id="9e2ae-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2ae-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e2ae-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2ae-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e2ae-127">INPUTS</span></span>

### <span data-ttu-id="9e2ae-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e2ae-128">None</span></span>

## <span data-ttu-id="9e2ae-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e2ae-129">OUTPUTS</span></span>

### <span data-ttu-id="9e2ae-130">Microsoft. Azure. Commands. platforming. models. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9e2ae-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="9e2ae-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e2ae-131">NOTES</span></span>

## <span data-ttu-id="9e2ae-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e2ae-132">RELATED LINKS</span></span>
