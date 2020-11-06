---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 04112d84acb8b18ef4251aae86b9bdd00924993a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525105"
---
# <span data-ttu-id="342e8-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="342e8-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="342e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="342e8-102">SYNOPSIS</span></span>
<span data-ttu-id="342e8-103">Pobiera reguły alertów.</span><span class="sxs-lookup"><span data-stu-id="342e8-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="342e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="342e8-104">SYNTAX</span></span>

### <span data-ttu-id="342e8-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="342e8-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342e8-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="342e8-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342e8-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="342e8-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342e8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="342e8-108">DESCRIPTION</span></span>
<span data-ttu-id="342e8-109">Polecenie cmdlet **Get-AzureRmAlertRule** pobiera regułę alertu przy użyciu jej nazwy lub identyfikatora URI lub wszystkich reguł alertów z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="342e8-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="342e8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="342e8-110">EXAMPLES</span></span>

### <span data-ttu-id="342e8-111">Przykład 1: uzyskiwanie reguł alertów dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="342e8-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="342e8-112">To polecenie pobiera wszystkie reguły alertów dla grupy zasobów o nazwie Default-Web-Central.</span><span class="sxs-lookup"><span data-stu-id="342e8-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="342e8-113">Dane wyjściowe nie zawierają szczegółów dotyczących reguł, ponieważ nie określono parametru *DetailedOutput* .</span><span class="sxs-lookup"><span data-stu-id="342e8-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="342e8-114">Przykład 2: uzyskiwanie reguły alertu według nazwy</span><span class="sxs-lookup"><span data-stu-id="342e8-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="342e8-115">To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="342e8-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="342e8-116">Ponieważ parametr *DetailedOutput* nie jest określony, dane wyjściowe zawierają tylko podstawowe informacje na temat reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="342e8-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="342e8-117">Przykład 3: uzyskiwanie reguły alertu według nazwy z danymi szczegółowymi</span><span class="sxs-lookup"><span data-stu-id="342e8-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="342e8-118">To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="342e8-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="342e8-119">Określono parametr *DetailedOutput* , więc dane wyjściowe są szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="342e8-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="342e8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="342e8-120">PARAMETERS</span></span>

### <span data-ttu-id="342e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342e8-121">-DefaultProfile</span></span>
<span data-ttu-id="342e8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="342e8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="342e8-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="342e8-123">-DetailedOutput</span></span>
<span data-ttu-id="342e8-124">Wyświetla wszystkie szczegóły w wynikach.</span><span class="sxs-lookup"><span data-stu-id="342e8-124">Displays full details in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342e8-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="342e8-125">-Name</span></span>
<span data-ttu-id="342e8-126">Określa nazwę reguły alertu, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="342e8-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="342e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="342e8-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="342e8-128">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342e8-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="342e8-129">-TargetResourceId</span></span>
<span data-ttu-id="342e8-130">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="342e8-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceUri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342e8-131">CommonParameters</span></span>
<span data-ttu-id="342e8-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="342e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342e8-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="342e8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342e8-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="342e8-134">INPUTS</span></span>

### <span data-ttu-id="342e8-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="342e8-135">None</span></span>
<span data-ttu-id="342e8-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="342e8-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="342e8-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="342e8-137">OUTPUTS</span></span>

### <span data-ttu-id="342e8-138">Lista<Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule></span><span class="sxs-lookup"><span data-stu-id="342e8-138">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule></span></span>

## <span data-ttu-id="342e8-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="342e8-139">NOTES</span></span>

## <span data-ttu-id="342e8-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="342e8-140">RELATED LINKS</span></span>

[<span data-ttu-id="342e8-141">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="342e8-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="342e8-142">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="342e8-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="342e8-143">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="342e8-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="342e8-144">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="342e8-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="342e8-145">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="342e8-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


