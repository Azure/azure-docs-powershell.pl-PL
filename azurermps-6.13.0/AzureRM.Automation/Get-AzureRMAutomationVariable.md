---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 7bd28149de46faa06420e87be8b83e7749ea248e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549456"
---
# <span data-ttu-id="c4ebc-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4ebc-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="c4ebc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ebc-103">Pobiera zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4ebc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4ebc-104">SYNTAX</span></span>

### <span data-ttu-id="c4ebc-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4ebc-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4ebc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c4ebc-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4ebc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c4ebc-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ebc-108">Polecenie cmdlet **Get-AzureRmAutomationVariable umożliwia pobranie** co najmniej jednej zmiennej automatyzacji Azure.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="c4ebc-109">Aby uzyskać określoną zmienną, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="c4ebc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4ebc-110">EXAMPLES</span></span>

### <span data-ttu-id="c4ebc-111">Przykład 1. Pobieranie zmiennej</span><span class="sxs-lookup"><span data-stu-id="c4ebc-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="c4ebc-112">Pierwsze polecenie pobiera zmienną automatyzacji o nazwie Variable06 na koncie o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="c4ebc-113">Polecenie zapisuje ten obiekt w zmiennej $Variable.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="c4ebc-114">Drugie polecenie używa standardowego zapisu kropkowego w celu odwoływania się do właściwości **value** $Variable.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="c4ebc-115">Polecenie zapisuje wartość w zmiennej $value.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="c4ebc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4ebc-116">PARAMETERS</span></span>

### <span data-ttu-id="c4ebc-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4ebc-117">-AutomationAccountName</span></span>
<span data-ttu-id="c4ebc-118">Określa nazwę konta automatyzacji zawierającego zmienne, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ebc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ebc-119">-DefaultProfile</span></span>
<span data-ttu-id="c4ebc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c4ebc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4ebc-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4ebc-121">-Name</span></span>
<span data-ttu-id="c4ebc-122">Określa nazwę zmiennej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ebc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ebc-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4ebc-124">Określa grupę zasobów, dla której ten aplet polecenia pobiera zmienne.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ebc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ebc-125">CommonParameters</span></span>
<span data-ttu-id="c4ebc-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ebc-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ebc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ebc-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4ebc-128">INPUTS</span></span>

### <span data-ttu-id="c4ebc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c4ebc-129">System.String</span></span>

## <span data-ttu-id="c4ebc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4ebc-130">OUTPUTS</span></span>

### <span data-ttu-id="c4ebc-131">Microsoft. Azure. Commands. Automation. model. zmienna</span><span class="sxs-lookup"><span data-stu-id="c4ebc-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="c4ebc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4ebc-132">NOTES</span></span>

## <span data-ttu-id="c4ebc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4ebc-133">RELATED LINKS</span></span>

[<span data-ttu-id="c4ebc-134">Nowe — AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4ebc-134">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="c4ebc-135">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4ebc-135">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="c4ebc-136">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4ebc-136">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


