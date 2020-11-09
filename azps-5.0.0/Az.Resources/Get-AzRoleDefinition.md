---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308827"
---
# <span data-ttu-id="d72ab-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d72ab-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="d72ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d72ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d72ab-103">Lista wszystkich ról usługi Azure RBAC dostępnych do przypisania.</span><span class="sxs-lookup"><span data-stu-id="d72ab-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="d72ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d72ab-104">SYNTAX</span></span>

### <span data-ttu-id="d72ab-105">RoleDefinitionNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d72ab-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d72ab-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d72ab-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d72ab-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="d72ab-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d72ab-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d72ab-108">DESCRIPTION</span></span>
<span data-ttu-id="d72ab-109">Użyj polecenia Get-AzRoleDefinition z określoną nazwą roli, aby wyświetlić jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="d72ab-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="d72ab-110">Aby sprawdzić poszczególne operacje, do których rola udziela dostępu, przejrzyj właściwości akcji i nienaruszonych ról.</span><span class="sxs-lookup"><span data-stu-id="d72ab-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="d72ab-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d72ab-111">EXAMPLES</span></span>

### <span data-ttu-id="d72ab-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d72ab-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="d72ab-113">Pobierz definicję roli czytelnika</span><span class="sxs-lookup"><span data-stu-id="d72ab-113">Get the Reader role definition</span></span>

### <span data-ttu-id="d72ab-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d72ab-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="d72ab-115">Lista wszystkich definicji ról RBAC</span><span class="sxs-lookup"><span data-stu-id="d72ab-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="d72ab-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d72ab-116">PARAMETERS</span></span>

### <span data-ttu-id="d72ab-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="d72ab-117">-Custom</span></span>
<span data-ttu-id="d72ab-118">Jeśli ta informacja jest określona, wyświetlane są tylko niestandardowe role utworzone w katalogu.</span><span class="sxs-lookup"><span data-stu-id="d72ab-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72ab-119">-DefaultProfile</span></span>
<span data-ttu-id="d72ab-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d72ab-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d72ab-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d72ab-121">-Id</span></span>
<span data-ttu-id="d72ab-122">Identyfikator definicji roli.</span><span class="sxs-lookup"><span data-stu-id="d72ab-122">Role definition Id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72ab-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d72ab-123">-Name</span></span>
<span data-ttu-id="d72ab-124">Nazwa definicji roli.</span><span class="sxs-lookup"><span data-stu-id="d72ab-124">Role definition name.</span></span>
<span data-ttu-id="d72ab-125">Dla przykładu czytelnik, współautor, współautor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72ab-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72ab-126">-Zakres</span><span class="sxs-lookup"><span data-stu-id="d72ab-126">-Scope</span></span>
<span data-ttu-id="d72ab-127">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="d72ab-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d72ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72ab-128">CommonParameters</span></span>
<span data-ttu-id="d72ab-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72ab-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d72ab-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72ab-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d72ab-131">INPUTS</span></span>

### <span data-ttu-id="d72ab-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d72ab-132">System.String</span></span>

### <span data-ttu-id="d72ab-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d72ab-133">System.Guid</span></span>

### <span data-ttu-id="d72ab-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d72ab-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d72ab-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d72ab-135">OUTPUTS</span></span>

### <span data-ttu-id="d72ab-136">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d72ab-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="d72ab-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d72ab-137">NOTES</span></span>
<span data-ttu-id="d72ab-138">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="d72ab-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d72ab-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d72ab-139">RELATED LINKS</span></span>

[<span data-ttu-id="d72ab-140">Nowe — AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d72ab-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="d72ab-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d72ab-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="d72ab-142">Nowe — AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d72ab-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="d72ab-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d72ab-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

