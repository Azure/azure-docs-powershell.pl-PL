---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2011b0ec99e2ef2287e5b74a08a11fdc1e4ef149
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525377"
---
# <span data-ttu-id="21d8f-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21d8f-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="21d8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="21d8f-103">Pobiera metadane modułów z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="21d8f-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21d8f-104">SYNTAX</span></span>

### <span data-ttu-id="21d8f-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21d8f-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21d8f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="21d8f-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21d8f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="21d8f-107">DESCRIPTION</span></span>
<span data-ttu-id="21d8f-108">Polecenie cmdlet **Get-AzureRmAutomationModule** pobiera metadane modułów z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="21d8f-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="21d8f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="21d8f-110">Przykład 1. Pobierz wszystkie moduły</span><span class="sxs-lookup"><span data-stu-id="21d8f-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="21d8f-111">To polecenie pobiera wszystkie moduły z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="21d8f-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="21d8f-112">Przykład 2: uzyskiwanie modułu</span><span class="sxs-lookup"><span data-stu-id="21d8f-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="21d8f-113">To polecenie Pobiera moduł o nazwie ContosoModule na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="21d8f-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="21d8f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21d8f-114">PARAMETERS</span></span>

### <span data-ttu-id="21d8f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="21d8f-115">-AutomationAccountName</span></span>
<span data-ttu-id="21d8f-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="21d8f-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d8f-117">-DefaultProfile</span></span>
<span data-ttu-id="21d8f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="21d8f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21d8f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21d8f-119">-Name</span></span>
<span data-ttu-id="21d8f-120">Określa nazwę modułu, dla którego to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="21d8f-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d8f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d8f-121">-ResourceGroupName</span></span>
<span data-ttu-id="21d8f-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="21d8f-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d8f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d8f-123">CommonParameters</span></span>
<span data-ttu-id="21d8f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d8f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d8f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d8f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d8f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21d8f-126">INPUTS</span></span>

### <span data-ttu-id="21d8f-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="21d8f-127">None</span></span>
<span data-ttu-id="21d8f-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="21d8f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21d8f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21d8f-129">OUTPUTS</span></span>

### <span data-ttu-id="21d8f-130">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="21d8f-130">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="21d8f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21d8f-131">NOTES</span></span>

## <span data-ttu-id="21d8f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21d8f-132">RELATED LINKS</span></span>

[<span data-ttu-id="21d8f-133">Nowe — AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21d8f-133">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="21d8f-134">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21d8f-134">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="21d8f-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21d8f-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


