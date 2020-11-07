---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717354"
---
# <span data-ttu-id="feabe-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="feabe-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="feabe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="feabe-102">SYNOPSIS</span></span>
<span data-ttu-id="feabe-103">Tworzy konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="feabe-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feabe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="feabe-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feabe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="feabe-105">DESCRIPTION</span></span>
<span data-ttu-id="feabe-106">Polecenie cmdlet **New-AzureRmAutomationAccount** tworzy konto usługi Azure Automation w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="feabe-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="feabe-107">Konto usługi Automation to kontener zasobów automatyzacji odizolowanych od zasobów innych kont automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="feabe-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="feabe-108">Zasoby automatyzacji obejmują elementy Runbook, konfiguracje (wymagane) konfiguracji stanu (DSC), zadania i zasoby.</span><span class="sxs-lookup"><span data-stu-id="feabe-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="feabe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="feabe-109">EXAMPLES</span></span>

### <span data-ttu-id="feabe-110">Przykład 1. Tworzenie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="feabe-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="feabe-111">To polecenie tworzy nowe konto usługi Automation o nazwie ContosoAutomationAccount w regionie wschód USA.</span><span class="sxs-lookup"><span data-stu-id="feabe-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="feabe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="feabe-112">PARAMETERS</span></span>

### <span data-ttu-id="feabe-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="feabe-113">-Location</span></span>
<span data-ttu-id="feabe-114">Określa lokalizację, w której to polecenie cmdlet tworzy konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="feabe-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="feabe-115">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="feabe-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="feabe-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="feabe-116">-Name</span></span>
<span data-ttu-id="feabe-117">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="feabe-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="feabe-118">-Plan</span><span class="sxs-lookup"><span data-stu-id="feabe-118">-Plan</span></span>
<span data-ttu-id="feabe-119">Określa plan konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="feabe-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="feabe-120">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="feabe-120">Valid values are:</span></span>

- <span data-ttu-id="feabe-121">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="feabe-121">Basic</span></span>
- <span data-ttu-id="feabe-122">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="feabe-122">Free</span></span>

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

### <span data-ttu-id="feabe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feabe-123">-ResourceGroupName</span></span>
<span data-ttu-id="feabe-124">Określa nazwę grupy zasobów, do której to polecenie cmdlet dodaje konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="feabe-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="feabe-125">-Tagi</span><span class="sxs-lookup"><span data-stu-id="feabe-125">-Tags</span></span>
<span data-ttu-id="feabe-126">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="feabe-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="feabe-127">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="feabe-127">For example:</span></span>

<span data-ttu-id="feabe-128">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="feabe-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="feabe-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feabe-129">-DefaultProfile</span></span>
<span data-ttu-id="feabe-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="feabe-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feabe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feabe-131">CommonParameters</span></span>
<span data-ttu-id="feabe-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feabe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feabe-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feabe-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feabe-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="feabe-134">INPUTS</span></span>

## <span data-ttu-id="feabe-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="feabe-135">OUTPUTS</span></span>

### <span data-ttu-id="feabe-136">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="feabe-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="feabe-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="feabe-137">NOTES</span></span>

## <span data-ttu-id="feabe-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="feabe-138">RELATED LINKS</span></span>

[<span data-ttu-id="feabe-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="feabe-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="feabe-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="feabe-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="feabe-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="feabe-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
