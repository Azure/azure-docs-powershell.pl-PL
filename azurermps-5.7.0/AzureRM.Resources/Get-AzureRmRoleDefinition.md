---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550560"
---
# <span data-ttu-id="87073-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="87073-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="87073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87073-102">SYNOPSIS</span></span>
<span data-ttu-id="87073-103">Lista wszystkich ról usługi Azure RBAC dostępnych do przypisania.</span><span class="sxs-lookup"><span data-stu-id="87073-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87073-104">SYNTAX</span></span>

### <span data-ttu-id="87073-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="87073-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87073-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87073-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87073-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="87073-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87073-108">Opis</span><span class="sxs-lookup"><span data-stu-id="87073-108">DESCRIPTION</span></span>
<span data-ttu-id="87073-109">Użyj polecenia Get-AzureRmRoleDefinition z określoną nazwą roli, aby wyświetlić jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="87073-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="87073-110">Aby sprawdzić poszczególne operacje, do których rola udziela dostępu, przejrzyj właściwości akcji i nienaruszonych ról.</span><span class="sxs-lookup"><span data-stu-id="87073-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="87073-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87073-111">EXAMPLES</span></span>

### <span data-ttu-id="87073-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87073-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="87073-113">Pobierz definicję roli czytelnika</span><span class="sxs-lookup"><span data-stu-id="87073-113">Get the Reader role definition</span></span>

### <span data-ttu-id="87073-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="87073-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="87073-115">Lista wszystkich definicji ról RBAC</span><span class="sxs-lookup"><span data-stu-id="87073-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="87073-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87073-116">PARAMETERS</span></span>

### <span data-ttu-id="87073-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="87073-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="87073-118">Jeśli jest określona, wyświetla wszystkie definicje ról.</span><span class="sxs-lookup"><span data-stu-id="87073-118">If specified, displays all role definitions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87073-119">-Custom</span><span class="sxs-lookup"><span data-stu-id="87073-119">-Custom</span></span>
<span data-ttu-id="87073-120">Jeśli ta informacja jest określona, wyświetlane są tylko niestandardowe role utworzone w katalogu.</span><span class="sxs-lookup"><span data-stu-id="87073-120">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87073-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87073-121">-DefaultProfile</span></span>
<span data-ttu-id="87073-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87073-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87073-123">-ID</span><span class="sxs-lookup"><span data-stu-id="87073-123">-Id</span></span>
<span data-ttu-id="87073-124">Identyfikator definicji roli.</span><span class="sxs-lookup"><span data-stu-id="87073-124">Role definition Id.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87073-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87073-125">-Name</span></span>
<span data-ttu-id="87073-126">Nazwa definicji roli.</span><span class="sxs-lookup"><span data-stu-id="87073-126">Role definition name.</span></span>
<span data-ttu-id="87073-127">Dla przykładu czytelnik, współautor, współautor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87073-127">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87073-128">-Zakres</span><span class="sxs-lookup"><span data-stu-id="87073-128">-Scope</span></span>
<span data-ttu-id="87073-129">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="87073-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87073-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87073-130">CommonParameters</span></span>
<span data-ttu-id="87073-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87073-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87073-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87073-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87073-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87073-133">INPUTS</span></span>

### <span data-ttu-id="87073-134">Ciąg</span><span class="sxs-lookup"><span data-stu-id="87073-134">String</span></span>
<span data-ttu-id="87073-135">Parametr "Scope" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="87073-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="87073-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87073-136">OUTPUTS</span></span>

### <span data-ttu-id="87073-137">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. zasoby. MODELES autoryzacji. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="87073-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="87073-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87073-138">NOTES</span></span>
<span data-ttu-id="87073-139">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="87073-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="87073-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87073-140">RELATED LINKS</span></span>

[<span data-ttu-id="87073-141">Nowe — AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="87073-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="87073-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="87073-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="87073-143">Nowe — AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="87073-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="87073-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="87073-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)
