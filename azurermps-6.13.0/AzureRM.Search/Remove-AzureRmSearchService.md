---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549272"
---
# <span data-ttu-id="35200-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="35200-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="35200-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35200-102">SYNOPSIS</span></span>
<span data-ttu-id="35200-103">Usuwanie usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="35200-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35200-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35200-104">SYNTAX</span></span>

### <span data-ttu-id="35200-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35200-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35200-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35200-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35200-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35200-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35200-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35200-108">DESCRIPTION</span></span>
<span data-ttu-id="35200-109">Polecenie cmdlet **Remove-AzureRmSearchService** usuwa usługę Azure Search ze wskazanym paramters.</span><span class="sxs-lookup"><span data-stu-id="35200-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="35200-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35200-110">EXAMPLES</span></span>

### <span data-ttu-id="35200-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35200-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="35200-112">W tym przykładzie jest usuwana usługa Azure Search.</span><span class="sxs-lookup"><span data-stu-id="35200-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="35200-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35200-113">PARAMETERS</span></span>

### <span data-ttu-id="35200-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35200-114">-DefaultProfile</span></span>
<span data-ttu-id="35200-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35200-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35200-116">-Force</span><span class="sxs-lookup"><span data-stu-id="35200-116">-Force</span></span>
<span data-ttu-id="35200-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="35200-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="35200-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35200-118">-InputObject</span></span>
<span data-ttu-id="35200-119">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="35200-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="35200-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35200-120">-Name</span></span>
<span data-ttu-id="35200-121">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="35200-121">Search Service name.</span></span>

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

### <span data-ttu-id="35200-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35200-122">-PassThru</span></span>
<span data-ttu-id="35200-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="35200-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="35200-124">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="35200-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="35200-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35200-125">-ResourceGroupName</span></span>
<span data-ttu-id="35200-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35200-126">Resource Group name.</span></span>

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

### <span data-ttu-id="35200-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35200-127">-ResourceId</span></span>
<span data-ttu-id="35200-128">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="35200-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="35200-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35200-129">-Confirm</span></span>
<span data-ttu-id="35200-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35200-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35200-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35200-131">-WhatIf</span></span>
<span data-ttu-id="35200-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35200-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35200-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35200-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35200-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35200-134">CommonParameters</span></span>
<span data-ttu-id="35200-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35200-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35200-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35200-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35200-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35200-137">INPUTS</span></span>

### <span data-ttu-id="35200-138">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="35200-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="35200-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="35200-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="35200-140">System. String</span><span class="sxs-lookup"><span data-stu-id="35200-140">System.String</span></span>

## <span data-ttu-id="35200-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35200-141">OUTPUTS</span></span>

### <span data-ttu-id="35200-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35200-142">System.Boolean</span></span>

## <span data-ttu-id="35200-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35200-143">NOTES</span></span>

## <span data-ttu-id="35200-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35200-144">RELATED LINKS</span></span>

[<span data-ttu-id="35200-145">Nowe — AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="35200-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="35200-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="35200-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="35200-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="35200-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

