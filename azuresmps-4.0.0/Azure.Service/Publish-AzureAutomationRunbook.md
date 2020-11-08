---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054851"
---
# <span data-ttu-id="14ee2-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ee2-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="14ee2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14ee2-102">SYNOPSIS</span></span>

<span data-ttu-id="14ee2-103">Umożliwia opublikowanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="14ee2-103">Publishes a runbook.</span></span>

## <span data-ttu-id="14ee2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14ee2-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="14ee2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14ee2-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="14ee2-106">Polecenie cmdlet **Publish-AzureAutomationRunbook** umożliwia publikowanie elementu Runbook do użycia w środowisku produkcyjnym usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="14ee2-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="14ee2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14ee2-107">EXAMPLES</span></span>

### <span data-ttu-id="14ee2-108">Przykład 1. publikowanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="14ee2-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="14ee2-109">To polecenie umożliwia opublikowanie elementu Runbook o nazwie Runbk01 na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="14ee2-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="14ee2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14ee2-110">PARAMETERS</span></span>

### <span data-ttu-id="14ee2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14ee2-111">-AutomationAccountName</span></span>
<span data-ttu-id="14ee2-112">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="14ee2-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="14ee2-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14ee2-113">-Name</span></span>
<span data-ttu-id="14ee2-114">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="14ee2-114">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14ee2-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="14ee2-115">-Profile</span></span>
<span data-ttu-id="14ee2-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14ee2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14ee2-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="14ee2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14ee2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ee2-118">CommonParameters</span></span>
<span data-ttu-id="14ee2-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14ee2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ee2-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ee2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ee2-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14ee2-121">INPUTS</span></span>

## <span data-ttu-id="14ee2-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14ee2-122">OUTPUTS</span></span>

## <span data-ttu-id="14ee2-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14ee2-123">NOTES</span></span>

## <span data-ttu-id="14ee2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14ee2-124">RELATED LINKS</span></span>

[<span data-ttu-id="14ee2-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ee2-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="14ee2-126">Nowe — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ee2-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="14ee2-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ee2-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="14ee2-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ee2-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="14ee2-129">Start — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="14ee2-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


