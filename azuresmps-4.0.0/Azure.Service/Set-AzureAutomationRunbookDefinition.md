---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055036"
---
# <span data-ttu-id="e4ac7-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="e4ac7-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="e4ac7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4ac7-102">SYNOPSIS</span></span>

<span data-ttu-id="e4ac7-103">Aktualizuje definicję wersji roboczej elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="e4ac7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4ac7-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4ac7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4ac7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e4ac7-106">Polecenie cmdlet **Set-AzureAutomationRunbookDefinition** aktualizuje definicję wersji roboczej elementu Runbook usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="e4ac7-107">Określ plik skryptu programu Windows PowerShell (. ps1) zawierający element Runbook, który stanie się wersją roboczą elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="e4ac7-108">Jeśli definicja wersji roboczej już istnieje, użyj parametru *overwrite* , aby wymusić zastąpienie istniejącej wersji roboczej polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="e4ac7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4ac7-109">EXAMPLES</span></span>

### <span data-ttu-id="e4ac7-110">Przykład 1. zastąpienie istniejącej definicji wersji roboczej elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="e4ac7-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="e4ac7-111">To polecenie zastępuje istniejącą definicję roboczą elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="e4ac7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4ac7-112">PARAMETERS</span></span>

### <span data-ttu-id="e4ac7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e4ac7-113">-AutomationAccountName</span></span>
<span data-ttu-id="e4ac7-114">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="e4ac7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4ac7-115">-Name</span></span>
<span data-ttu-id="e4ac7-116">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-116">Specifies a name.</span></span>

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

### <span data-ttu-id="e4ac7-117">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e4ac7-117">-Overwrite</span></span>
<span data-ttu-id="e4ac7-118">Wskazuje, czy ma zostać zastąpiona istniejąca definicja robocza.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-118">Indicates whether to overwrite an existing draft definition.</span></span>

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

### <span data-ttu-id="e4ac7-119">-Path</span><span class="sxs-lookup"><span data-stu-id="e4ac7-119">-Path</span></span>
<span data-ttu-id="e4ac7-120">Określa ścieżkę do elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ac7-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="e4ac7-121">-Profile</span></span>
<span data-ttu-id="e4ac7-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4ac7-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4ac7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ac7-124">CommonParameters</span></span>
<span data-ttu-id="e4ac7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ac7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ac7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ac7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ac7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4ac7-127">INPUTS</span></span>

## <span data-ttu-id="e4ac7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4ac7-128">OUTPUTS</span></span>

### <span data-ttu-id="e4ac7-129">Microsoft. Azure. Commands. Automation. model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="e4ac7-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="e4ac7-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4ac7-130">NOTES</span></span>

## <span data-ttu-id="e4ac7-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4ac7-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4ac7-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="e4ac7-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


