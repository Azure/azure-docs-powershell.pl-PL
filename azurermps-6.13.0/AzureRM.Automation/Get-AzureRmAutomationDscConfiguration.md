---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 10e04dc24c34ba60186c8166e2626524fcc60a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524650"
---
# <span data-ttu-id="00105-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00105-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="00105-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00105-102">SYNOPSIS</span></span>
<span data-ttu-id="00105-103">Umożliwia pobieranie konfiguracji DSC z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="00105-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00105-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00105-104">SYNTAX</span></span>

### <span data-ttu-id="00105-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="00105-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00105-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="00105-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00105-107">Opis</span><span class="sxs-lookup"><span data-stu-id="00105-107">DESCRIPTION</span></span>
<span data-ttu-id="00105-108">Polecenie cmdlet **Get-AzureRmAutomationDscConfiguration** pobiera konfiguracje konfiguracji stanu żądanego (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="00105-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="00105-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00105-109">EXAMPLES</span></span>

### <span data-ttu-id="00105-110">Przykład 1: uzyskiwanie wszystkich konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="00105-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="00105-111">To polecenie pobiera metadane wszystkich konfiguracji DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00105-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="00105-112">Przykład 2: Uzyskiwanie konfiguracji DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="00105-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="00105-113">To polecenie pobiera metadane konfiguracji DSC o nazwie moja konfiguracja na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00105-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="00105-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00105-114">PARAMETERS</span></span>

### <span data-ttu-id="00105-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00105-115">-AutomationAccountName</span></span>
<span data-ttu-id="00105-116">Określa nazwę konta automatyzacji zawierającego konfiguracje DSC, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00105-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="00105-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00105-117">-DefaultProfile</span></span>
<span data-ttu-id="00105-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="00105-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00105-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00105-119">-Name</span></span>
<span data-ttu-id="00105-120">Określa nazwę konfiguracji DSC, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00105-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00105-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00105-121">-ResourceGroupName</span></span>
<span data-ttu-id="00105-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet ma pobierać konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="00105-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="00105-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00105-123">CommonParameters</span></span>
<span data-ttu-id="00105-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00105-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00105-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00105-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00105-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00105-126">INPUTS</span></span>

### <span data-ttu-id="00105-127">System. String</span><span class="sxs-lookup"><span data-stu-id="00105-127">System.String</span></span>

## <span data-ttu-id="00105-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00105-128">OUTPUTS</span></span>

### <span data-ttu-id="00105-129">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00105-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="00105-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00105-130">NOTES</span></span>

## <span data-ttu-id="00105-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00105-131">RELATED LINKS</span></span>

[<span data-ttu-id="00105-132">Eksportowanie — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00105-132">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="00105-133">Import — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00105-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


