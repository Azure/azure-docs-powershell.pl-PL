---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 6bf44f78c763c0150e31423acd9e3594e1baa717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708377"
---
# <span data-ttu-id="00e20-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00e20-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="00e20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00e20-102">SYNOPSIS</span></span>
<span data-ttu-id="00e20-103">Lista wszystkich ról usługi Azure RBAC dostępnych do przypisania.</span><span class="sxs-lookup"><span data-stu-id="00e20-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="00e20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00e20-104">SYNTAX</span></span>

### <span data-ttu-id="00e20-105">RoleDefinitionNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="00e20-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00e20-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00e20-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00e20-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="00e20-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00e20-108">Opis</span><span class="sxs-lookup"><span data-stu-id="00e20-108">DESCRIPTION</span></span>
<span data-ttu-id="00e20-109">Użyj polecenia Get-AzRoleDefinition z określoną nazwą roli, aby wyświetlić jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="00e20-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="00e20-110">Aby sprawdzić poszczególne operacje, do których rola udziela dostępu, przejrzyj właściwości akcji i nienaruszonych ról.</span><span class="sxs-lookup"><span data-stu-id="00e20-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="00e20-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00e20-111">EXAMPLES</span></span>

### <span data-ttu-id="00e20-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00e20-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="00e20-113">Pobierz definicję roli czytelnika</span><span class="sxs-lookup"><span data-stu-id="00e20-113">Get the Reader role definition</span></span>

### <span data-ttu-id="00e20-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="00e20-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="00e20-115">Lista wszystkich definicji ról RBAC</span><span class="sxs-lookup"><span data-stu-id="00e20-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="00e20-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00e20-116">PARAMETERS</span></span>

### <span data-ttu-id="00e20-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="00e20-117">-Custom</span></span>
<span data-ttu-id="00e20-118">Jeśli ta informacja jest określona, wyświetlane są tylko niestandardowe role utworzone w katalogu.</span><span class="sxs-lookup"><span data-stu-id="00e20-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="00e20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e20-119">-DefaultProfile</span></span>
<span data-ttu-id="00e20-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="00e20-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00e20-121">-ID</span><span class="sxs-lookup"><span data-stu-id="00e20-121">-Id</span></span>
<span data-ttu-id="00e20-122">Identyfikator definicji roli.</span><span class="sxs-lookup"><span data-stu-id="00e20-122">Role definition Id.</span></span>

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

### <span data-ttu-id="00e20-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00e20-123">-Name</span></span>
<span data-ttu-id="00e20-124">Nazwa definicji roli.</span><span class="sxs-lookup"><span data-stu-id="00e20-124">Role definition name.</span></span>
<span data-ttu-id="00e20-125">Dla przykładu czytelnik, współautor, współautor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="00e20-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="00e20-126">-Zakres</span><span class="sxs-lookup"><span data-stu-id="00e20-126">-Scope</span></span>
<span data-ttu-id="00e20-127">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="00e20-127">Role definition scope.</span></span>

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

### <span data-ttu-id="00e20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e20-128">CommonParameters</span></span>
<span data-ttu-id="00e20-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e20-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e20-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e20-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00e20-131">INPUTS</span></span>

### <span data-ttu-id="00e20-132">System. String</span><span class="sxs-lookup"><span data-stu-id="00e20-132">System.String</span></span>

### <span data-ttu-id="00e20-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="00e20-133">System.Guid</span></span>

### <span data-ttu-id="00e20-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="00e20-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="00e20-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00e20-135">OUTPUTS</span></span>

### <span data-ttu-id="00e20-136">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00e20-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="00e20-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00e20-137">NOTES</span></span>
<span data-ttu-id="00e20-138">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="00e20-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="00e20-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00e20-139">RELATED LINKS</span></span>

[<span data-ttu-id="00e20-140">Nowe — AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="00e20-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="00e20-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="00e20-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="00e20-142">Nowe — AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00e20-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="00e20-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00e20-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)
