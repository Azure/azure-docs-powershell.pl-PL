---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: 9db953cf4c02497fd3056a57ed7b71a78687411d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719552"
---
# <span data-ttu-id="1e27a-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1e27a-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="1e27a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e27a-102">SYNOPSIS</span></span>
<span data-ttu-id="1e27a-103">Lista wszystkich ról usługi Azure RBAC dostępnych do przypisania.</span><span class="sxs-lookup"><span data-stu-id="1e27a-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e27a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e27a-104">SYNTAX</span></span>

### <span data-ttu-id="1e27a-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e27a-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e27a-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e27a-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e27a-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e27a-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e27a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e27a-108">DESCRIPTION</span></span>
<span data-ttu-id="1e27a-109">Użyj polecenia Get-AzureRmRoleDefinition z określoną nazwą roli, aby wyświetlić jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="1e27a-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="1e27a-110">Aby sprawdzić poszczególne operacje, do których rola udziela dostępu, przejrzyj właściwości akcji i nienaruszonych ról.</span><span class="sxs-lookup"><span data-stu-id="1e27a-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="1e27a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e27a-111">EXAMPLES</span></span>

### <span data-ttu-id="1e27a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e27a-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="1e27a-113">Pobierz definicję roli czytelnika</span><span class="sxs-lookup"><span data-stu-id="1e27a-113">Get the Reader role definition</span></span>

### <span data-ttu-id="1e27a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1e27a-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="1e27a-115">Lista wszystkich definicji ról RBAC</span><span class="sxs-lookup"><span data-stu-id="1e27a-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="1e27a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e27a-116">PARAMETERS</span></span>

### <span data-ttu-id="1e27a-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="1e27a-117">-Custom</span></span>
<span data-ttu-id="1e27a-118">Jeśli ta informacja jest określona, wyświetlane są tylko niestandardowe role utworzone w katalogu.</span><span class="sxs-lookup"><span data-stu-id="1e27a-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="1e27a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e27a-119">-DefaultProfile</span></span>
<span data-ttu-id="1e27a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1e27a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e27a-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1e27a-121">-Id</span></span>
<span data-ttu-id="1e27a-122">Identyfikator definicji roli.</span><span class="sxs-lookup"><span data-stu-id="1e27a-122">Role definition Id.</span></span>

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

### <span data-ttu-id="1e27a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e27a-123">-Name</span></span>
<span data-ttu-id="1e27a-124">Nazwa definicji roli.</span><span class="sxs-lookup"><span data-stu-id="1e27a-124">Role definition name.</span></span>
<span data-ttu-id="1e27a-125">Dla przykładu czytelnik, współautor, współautor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1e27a-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="1e27a-126">-Zakres</span><span class="sxs-lookup"><span data-stu-id="1e27a-126">-Scope</span></span>
<span data-ttu-id="1e27a-127">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="1e27a-127">Role definition scope.</span></span>

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

### <span data-ttu-id="1e27a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e27a-128">CommonParameters</span></span>
<span data-ttu-id="1e27a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e27a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e27a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e27a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e27a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e27a-131">INPUTS</span></span>

### <span data-ttu-id="1e27a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e27a-132">System.String</span></span>
<span data-ttu-id="1e27a-133">Parametry: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1e27a-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="1e27a-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1e27a-134">System.Guid</span></span>

### <span data-ttu-id="1e27a-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1e27a-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1e27a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e27a-136">OUTPUTS</span></span>

### <span data-ttu-id="1e27a-137">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1e27a-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="1e27a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e27a-138">NOTES</span></span>
<span data-ttu-id="1e27a-139">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="1e27a-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1e27a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e27a-140">RELATED LINKS</span></span>

[<span data-ttu-id="1e27a-141">Nowe — AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1e27a-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="1e27a-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1e27a-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="1e27a-143">Nowe — AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1e27a-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="1e27a-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1e27a-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

