---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055447"
---
# <span data-ttu-id="3cea4-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3cea4-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="3cea4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cea4-102">SYNOPSIS</span></span>

<span data-ttu-id="3cea4-103">Umożliwia usunięcie modułu z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3cea4-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="3cea4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cea4-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3cea4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cea4-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3cea4-106">Polecenie cmdlet **Remove-AzureAutomationModule** umożliwia usunięcie konta usługi Automation z usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3cea4-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="3cea4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cea4-107">EXAMPLES</span></span>

### <span data-ttu-id="3cea4-108">Przykład 1: usuwanie modułu</span><span class="sxs-lookup"><span data-stu-id="3cea4-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="3cea4-109">To polecenie umożliwia usunięcie modułu o nazwie ContosoModule z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3cea4-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3cea4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cea4-110">PARAMETERS</span></span>

### <span data-ttu-id="3cea4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3cea4-111">-AutomationAccountName</span></span>
<span data-ttu-id="3cea4-112">Określa nazwę konta automatyzacji z modułem.</span><span class="sxs-lookup"><span data-stu-id="3cea4-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="3cea4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3cea4-113">-Force</span></span>
<span data-ttu-id="3cea4-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3cea4-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cea4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cea4-115">-Name</span></span>
<span data-ttu-id="3cea4-116">Określa nazwę modułu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="3cea4-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="3cea4-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="3cea4-117">-Profile</span></span>
<span data-ttu-id="3cea4-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cea4-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3cea4-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3cea4-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3cea4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cea4-120">CommonParameters</span></span>
<span data-ttu-id="3cea4-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cea4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cea4-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cea4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cea4-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cea4-123">INPUTS</span></span>

## <span data-ttu-id="3cea4-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cea4-124">OUTPUTS</span></span>

## <span data-ttu-id="3cea4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cea4-125">NOTES</span></span>

## <span data-ttu-id="3cea4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cea4-126">RELATED LINKS</span></span>

[<span data-ttu-id="3cea4-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3cea4-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="3cea4-128">Nowe — AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3cea4-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="3cea4-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3cea4-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


