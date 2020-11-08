---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055135"
---
# <span data-ttu-id="af06d-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="af06d-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="af06d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af06d-102">SYNOPSIS</span></span>

<span data-ttu-id="af06d-103">Usuwa zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="af06d-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="af06d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af06d-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="af06d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af06d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="af06d-106">Polecenie cmdlet **Remove-AzureAutomationVariable** usuwa zmienną z usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="af06d-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="af06d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af06d-107">EXAMPLES</span></span>

### <span data-ttu-id="af06d-108">Przykład 1. Usuń zmienną</span><span class="sxs-lookup"><span data-stu-id="af06d-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="af06d-109">To polecenie usuwa zmienną o nazwie MyStringVariable na koncie automatyzacji o nazwie Contoso17 bez monitowania o weryfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="af06d-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="af06d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af06d-110">PARAMETERS</span></span>

### <span data-ttu-id="af06d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af06d-111">-AutomationAccountName</span></span>
<span data-ttu-id="af06d-112">Określa nazwę konta automatyzacji ze zmienną.</span><span class="sxs-lookup"><span data-stu-id="af06d-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="af06d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="af06d-113">-Force</span></span>
<span data-ttu-id="af06d-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="af06d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af06d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af06d-115">-Name</span></span>
<span data-ttu-id="af06d-116">Określa nazwę zmiennej.</span><span class="sxs-lookup"><span data-stu-id="af06d-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="af06d-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="af06d-117">-Profile</span></span>
<span data-ttu-id="af06d-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af06d-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af06d-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="af06d-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af06d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af06d-120">CommonParameters</span></span>
<span data-ttu-id="af06d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af06d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af06d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af06d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af06d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af06d-123">INPUTS</span></span>

## <span data-ttu-id="af06d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af06d-124">OUTPUTS</span></span>

## <span data-ttu-id="af06d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af06d-125">NOTES</span></span>

## <span data-ttu-id="af06d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af06d-126">RELATED LINKS</span></span>

[<span data-ttu-id="af06d-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="af06d-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="af06d-128">Nowe — AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="af06d-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="af06d-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="af06d-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


