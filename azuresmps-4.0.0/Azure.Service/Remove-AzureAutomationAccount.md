---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055461"
---
# <span data-ttu-id="6bbf8-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6bbf8-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="6bbf8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bbf8-102">SYNOPSIS</span></span>

<span data-ttu-id="6bbf8-103">Usuwa konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="6bbf8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bbf8-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6bbf8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6bbf8-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6bbf8-106">Polecenie cmdlet **Remove-AzureAutomationAccount** umożliwia usunięcie konta z usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6bbf8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bbf8-107">EXAMPLES</span></span>

### <span data-ttu-id="6bbf8-108">Przykład 1: usuwanie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="6bbf8-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="6bbf8-109">To polecenie usuwa konto usługi Automation o nazwie MyAutomationAccount bez monitowania o weryfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="6bbf8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bbf8-110">PARAMETERS</span></span>

### <span data-ttu-id="6bbf8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6bbf8-111">-Force</span></span>
<span data-ttu-id="6bbf8-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6bbf8-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bbf8-113">-Name</span></span>
<span data-ttu-id="6bbf8-114">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-114">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbf8-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="6bbf8-115">-Profile</span></span>
<span data-ttu-id="6bbf8-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6bbf8-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6bbf8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbf8-118">CommonParameters</span></span>
<span data-ttu-id="6bbf8-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbf8-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bbf8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbf8-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bbf8-121">INPUTS</span></span>

## <span data-ttu-id="6bbf8-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bbf8-122">OUTPUTS</span></span>

## <span data-ttu-id="6bbf8-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bbf8-123">NOTES</span></span>

## <span data-ttu-id="6bbf8-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bbf8-124">RELATED LINKS</span></span>

[<span data-ttu-id="6bbf8-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6bbf8-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="6bbf8-126">Nowe — AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6bbf8-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


