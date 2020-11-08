---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055334"
---
# <span data-ttu-id="deaa9-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="deaa9-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="deaa9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="deaa9-102">SYNOPSIS</span></span>

<span data-ttu-id="deaa9-103">Pobierz moduł usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="deaa9-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="deaa9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="deaa9-104">SYNTAX</span></span>

### <span data-ttu-id="deaa9-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="deaa9-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="deaa9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="deaa9-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="deaa9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="deaa9-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="deaa9-108">Polecenie cmdlet **Get-AzureAutomationModule** pobiera co najmniej jeden moduł automatyzacji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="deaa9-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="deaa9-109">Domyślnie zwracane są wszystkie moduły.</span><span class="sxs-lookup"><span data-stu-id="deaa9-109">By default, all modules are returned.</span></span>
<span data-ttu-id="deaa9-110">Aby uzyskać określony moduł, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="deaa9-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="deaa9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="deaa9-111">EXAMPLES</span></span>

### <span data-ttu-id="deaa9-112">Przykład 1. Pobierz wszystkie moduły</span><span class="sxs-lookup"><span data-stu-id="deaa9-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="deaa9-113">To polecenie pobiera wszystkie moduły z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="deaa9-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="deaa9-114">Przykład 2: uzyskiwanie modułu</span><span class="sxs-lookup"><span data-stu-id="deaa9-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="deaa9-115">To polecenie Pobiera moduł o nazwie ContosoModule na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="deaa9-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="deaa9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="deaa9-116">PARAMETERS</span></span>

### <span data-ttu-id="deaa9-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="deaa9-117">-AutomationAccountName</span></span>
<span data-ttu-id="deaa9-118">Określa nazwę konta automatyzacji, którego element Runbook należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="deaa9-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deaa9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="deaa9-119">-Name</span></span>
<span data-ttu-id="deaa9-120">Określa nazwę modułu, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="deaa9-120">Specifies the name of a module to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deaa9-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="deaa9-121">-Profile</span></span>
<span data-ttu-id="deaa9-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deaa9-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="deaa9-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="deaa9-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deaa9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deaa9-124">CommonParameters</span></span>
<span data-ttu-id="deaa9-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deaa9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deaa9-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deaa9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deaa9-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="deaa9-127">INPUTS</span></span>

## <span data-ttu-id="deaa9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="deaa9-128">OUTPUTS</span></span>

### <span data-ttu-id="deaa9-129">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="deaa9-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="deaa9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="deaa9-130">NOTES</span></span>

## <span data-ttu-id="deaa9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="deaa9-131">RELATED LINKS</span></span>

[<span data-ttu-id="deaa9-132">Nowe — AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="deaa9-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="deaa9-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="deaa9-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="deaa9-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="deaa9-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


