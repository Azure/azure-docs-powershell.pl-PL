---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 245cbce2516dcb26502313bcac35dd35b957f94d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708238"
---
# <span data-ttu-id="81d6a-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="81d6a-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="81d6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="81d6a-103">Usuwanie usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="81d6a-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="81d6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81d6a-104">SYNTAX</span></span>

### <span data-ttu-id="81d6a-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="81d6a-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d6a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d6a-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d6a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d6a-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d6a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="81d6a-108">DESCRIPTION</span></span>
<span data-ttu-id="81d6a-109">Polecenie cmdlet **Remove-AzSearchService** usuwa usługę Azure Search ze wskazanym paramters.</span><span class="sxs-lookup"><span data-stu-id="81d6a-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="81d6a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81d6a-110">EXAMPLES</span></span>

### <span data-ttu-id="81d6a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81d6a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="81d6a-112">W tym przykładzie jest usuwana usługa Azure Search.</span><span class="sxs-lookup"><span data-stu-id="81d6a-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="81d6a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81d6a-113">PARAMETERS</span></span>

### <span data-ttu-id="81d6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d6a-114">-DefaultProfile</span></span>
<span data-ttu-id="81d6a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81d6a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d6a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="81d6a-116">-Force</span></span>
<span data-ttu-id="81d6a-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81d6a-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81d6a-118">-InputObject</span></span>
<span data-ttu-id="81d6a-119">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="81d6a-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81d6a-120">-Name</span></span>
<span data-ttu-id="81d6a-121">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="81d6a-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81d6a-122">-PassThru</span></span>
<span data-ttu-id="81d6a-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="81d6a-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="81d6a-124">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="81d6a-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d6a-125">-ResourceGroupName</span></span>
<span data-ttu-id="81d6a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81d6a-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81d6a-127">-ResourceId</span></span>
<span data-ttu-id="81d6a-128">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="81d6a-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81d6a-129">-Confirm</span></span>
<span data-ttu-id="81d6a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d6a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d6a-131">-WhatIf</span></span>
<span data-ttu-id="81d6a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d6a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81d6a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d6a-134">CommonParameters</span></span>
<span data-ttu-id="81d6a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d6a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d6a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d6a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81d6a-137">INPUTS</span></span>

### <span data-ttu-id="81d6a-138">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="81d6a-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="81d6a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="81d6a-139">System.String</span></span>

## <span data-ttu-id="81d6a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81d6a-140">OUTPUTS</span></span>

### <span data-ttu-id="81d6a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81d6a-141">System.Boolean</span></span>

## <span data-ttu-id="81d6a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81d6a-142">NOTES</span></span>

## <span data-ttu-id="81d6a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81d6a-143">RELATED LINKS</span></span>

[<span data-ttu-id="81d6a-144">Nowe — AzSearchService</span><span class="sxs-lookup"><span data-stu-id="81d6a-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="81d6a-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="81d6a-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="81d6a-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="81d6a-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

