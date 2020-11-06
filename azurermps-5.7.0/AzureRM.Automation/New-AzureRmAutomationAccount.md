---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527137"
---
# <span data-ttu-id="3d600-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3d600-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="3d600-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d600-102">SYNOPSIS</span></span>
<span data-ttu-id="3d600-103">Tworzy konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="3d600-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d600-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d600-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d600-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d600-105">DESCRIPTION</span></span>
<span data-ttu-id="3d600-106">Polecenie cmdlet **New-AzureRmAutomationAccount** tworzy konto usługi Azure Automation w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d600-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="3d600-107">Konto usługi Automation to kontener zasobów automatyzacji odizolowanych od zasobów innych kont automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3d600-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="3d600-108">Zasoby automatyzacji obejmują elementy Runbook, konfiguracje (wymagane) konfiguracji stanu (DSC), zadania i zasoby.</span><span class="sxs-lookup"><span data-stu-id="3d600-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="3d600-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d600-109">EXAMPLES</span></span>

### <span data-ttu-id="3d600-110">Przykład 1. Tworzenie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="3d600-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3d600-111">To polecenie tworzy nowe konto usługi Automation o nazwie ContosoAutomationAccount w regionie wschód USA.</span><span class="sxs-lookup"><span data-stu-id="3d600-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="3d600-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d600-112">PARAMETERS</span></span>

### <span data-ttu-id="3d600-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d600-113">-DefaultProfile</span></span>
<span data-ttu-id="3d600-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3d600-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d600-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3d600-115">-Location</span></span>
<span data-ttu-id="3d600-116">Określa lokalizację, w której to polecenie cmdlet tworzy konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3d600-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="3d600-117">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="3d600-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d600-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d600-118">-Name</span></span>
<span data-ttu-id="3d600-119">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3d600-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d600-120">-Plan</span><span class="sxs-lookup"><span data-stu-id="3d600-120">-Plan</span></span>
<span data-ttu-id="3d600-121">Określa plan konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3d600-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="3d600-122">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3d600-122">Valid values are:</span></span>

- <span data-ttu-id="3d600-123">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="3d600-123">Basic</span></span>
- <span data-ttu-id="3d600-124">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="3d600-124">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d600-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d600-125">-ResourceGroupName</span></span>
<span data-ttu-id="3d600-126">Określa nazwę grupy zasobów, do której to polecenie cmdlet dodaje konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="3d600-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="3d600-127">-Tagi</span><span class="sxs-lookup"><span data-stu-id="3d600-127">-Tags</span></span>
<span data-ttu-id="3d600-128">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3d600-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3d600-129">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="3d600-129">For example:</span></span>

<span data-ttu-id="3d600-130">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="3d600-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d600-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d600-131">CommonParameters</span></span>
<span data-ttu-id="3d600-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d600-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d600-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d600-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d600-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d600-134">INPUTS</span></span>

### <span data-ttu-id="3d600-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3d600-135">None</span></span>
<span data-ttu-id="3d600-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3d600-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d600-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d600-137">OUTPUTS</span></span>

### <span data-ttu-id="3d600-138">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3d600-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="3d600-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d600-139">NOTES</span></span>

## <span data-ttu-id="3d600-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d600-140">RELATED LINKS</span></span>

[<span data-ttu-id="3d600-141">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3d600-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="3d600-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3d600-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="3d600-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3d600-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
