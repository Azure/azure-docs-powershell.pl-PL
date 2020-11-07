---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2ed40d0ee0698c8e0ee8d4a1c443db32c843ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716461"
---
# <span data-ttu-id="377a8-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="377a8-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="377a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="377a8-102">SYNOPSIS</span></span>
<span data-ttu-id="377a8-103">Pobiera metadane modułów z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="377a8-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="377a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="377a8-104">SYNTAX</span></span>

### <span data-ttu-id="377a8-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="377a8-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="377a8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="377a8-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="377a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="377a8-107">DESCRIPTION</span></span>
<span data-ttu-id="377a8-108">Polecenie cmdlet **Get-AzureRmAutomationModule** pobiera metadane modułów z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="377a8-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="377a8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="377a8-109">EXAMPLES</span></span>

### <span data-ttu-id="377a8-110">Przykład 1. Pobierz wszystkie moduły</span><span class="sxs-lookup"><span data-stu-id="377a8-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="377a8-111">To polecenie pobiera wszystkie moduły z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="377a8-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="377a8-112">Przykład 2: uzyskiwanie modułu</span><span class="sxs-lookup"><span data-stu-id="377a8-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="377a8-113">To polecenie Pobiera moduł o nazwie ContosoModule na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="377a8-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="377a8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="377a8-114">PARAMETERS</span></span>

### <span data-ttu-id="377a8-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="377a8-115">-AutomationAccountName</span></span>
<span data-ttu-id="377a8-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="377a8-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="377a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377a8-117">-DefaultProfile</span></span>
<span data-ttu-id="377a8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="377a8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="377a8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="377a8-119">-Name</span></span>
<span data-ttu-id="377a8-120">Określa nazwę modułu, dla którego to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="377a8-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="377a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="377a8-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera metadane modułu.</span><span class="sxs-lookup"><span data-stu-id="377a8-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="377a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377a8-123">CommonParameters</span></span>
<span data-ttu-id="377a8-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377a8-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377a8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377a8-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="377a8-126">INPUTS</span></span>

### <span data-ttu-id="377a8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="377a8-127">System.String</span></span>

## <span data-ttu-id="377a8-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="377a8-128">OUTPUTS</span></span>

### <span data-ttu-id="377a8-129">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="377a8-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="377a8-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="377a8-130">NOTES</span></span>

## <span data-ttu-id="377a8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="377a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="377a8-132">Nowe — AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="377a8-132">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="377a8-133">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="377a8-133">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="377a8-134">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="377a8-134">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


