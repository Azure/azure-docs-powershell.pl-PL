---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710541"
---
# <span data-ttu-id="87c06-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="87c06-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="87c06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87c06-102">SYNOPSIS</span></span>
<span data-ttu-id="87c06-103">Tworzy konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="87c06-103">Creates an Automation account.</span></span>

## <span data-ttu-id="87c06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87c06-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87c06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87c06-105">DESCRIPTION</span></span>
<span data-ttu-id="87c06-106">Polecenie cmdlet **New-AzAutomationAccount** tworzy konto usługi Azure Automation w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="87c06-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="87c06-107">Konto usługi Automation to kontener zasobów automatyzacji odizolowanych od zasobów innych kont automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="87c06-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="87c06-108">Zasoby automatyzacji obejmują elementy Runbook, konfiguracje (wymagane) konfiguracji stanu (DSC), zadania i zasoby.</span><span class="sxs-lookup"><span data-stu-id="87c06-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="87c06-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87c06-109">EXAMPLES</span></span>

### <span data-ttu-id="87c06-110">Przykład 1. Tworzenie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="87c06-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="87c06-111">To polecenie tworzy nowe konto usługi Automation o nazwie ContosoAutomationAccount w regionie wschód USA.</span><span class="sxs-lookup"><span data-stu-id="87c06-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="87c06-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87c06-112">PARAMETERS</span></span>

### <span data-ttu-id="87c06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c06-113">-DefaultProfile</span></span>
<span data-ttu-id="87c06-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87c06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87c06-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="87c06-115">-Location</span></span>
<span data-ttu-id="87c06-116">Określa lokalizację, w której to polecenie cmdlet tworzy konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="87c06-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="87c06-117">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="87c06-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c06-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87c06-118">-Name</span></span>
<span data-ttu-id="87c06-119">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="87c06-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c06-120">-Plan</span><span class="sxs-lookup"><span data-stu-id="87c06-120">-Plan</span></span>
<span data-ttu-id="87c06-121">Określa plan konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="87c06-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="87c06-122">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="87c06-122">Valid values are:</span></span>
- <span data-ttu-id="87c06-123">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="87c06-123">Basic</span></span>
- <span data-ttu-id="87c06-124">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="87c06-124">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c06-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c06-125">-ResourceGroupName</span></span>
<span data-ttu-id="87c06-126">Określa nazwę grupy zasobów, do której to polecenie cmdlet dodaje konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="87c06-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="87c06-127">-Tagi</span><span class="sxs-lookup"><span data-stu-id="87c06-127">-Tags</span></span>
<span data-ttu-id="87c06-128">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="87c06-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="87c06-129">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="87c06-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c06-130">CommonParameters</span></span>
<span data-ttu-id="87c06-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c06-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c06-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c06-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87c06-133">INPUTS</span></span>

### <span data-ttu-id="87c06-134">System. String</span><span class="sxs-lookup"><span data-stu-id="87c06-134">System.String</span></span>

### <span data-ttu-id="87c06-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="87c06-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="87c06-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87c06-136">OUTPUTS</span></span>

### <span data-ttu-id="87c06-137">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="87c06-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="87c06-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87c06-138">NOTES</span></span>

## <span data-ttu-id="87c06-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87c06-139">RELATED LINKS</span></span>

[<span data-ttu-id="87c06-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="87c06-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="87c06-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="87c06-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="87c06-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="87c06-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
