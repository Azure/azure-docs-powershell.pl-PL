---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055446"
---
# <span data-ttu-id="fe4b1-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe4b1-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="fe4b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe4b1-102">SYNOPSIS</span></span>

<span data-ttu-id="fe4b1-103">Usuwa poświadczenie z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="fe4b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe4b1-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe4b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe4b1-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="fe4b1-106">Polecenie cmdlet **Remove-AzureAutomationCredential** usuwa poświadczenia z usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="fe4b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe4b1-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4b1-108">Przykład 1: usuwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="fe4b1-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="fe4b1-109">To polecenie usuwa poświadczenia o nazwie moje poświadczenia na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="fe4b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe4b1-110">PARAMETERS</span></span>

### <span data-ttu-id="fe4b1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fe4b1-111">-AutomationAccountName</span></span>
<span data-ttu-id="fe4b1-112">Określa nazwę konta automatyzacji z poświadczeniami.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="fe4b1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fe4b1-113">-Force</span></span>
<span data-ttu-id="fe4b1-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe4b1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe4b1-115">-Name</span></span>
<span data-ttu-id="fe4b1-116">Określa nazwę poświadczenia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="fe4b1-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="fe4b1-117">-Profile</span></span>
<span data-ttu-id="fe4b1-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe4b1-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe4b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4b1-120">CommonParameters</span></span>
<span data-ttu-id="fe4b1-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4b1-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe4b1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4b1-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe4b1-123">INPUTS</span></span>

## <span data-ttu-id="fe4b1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe4b1-124">OUTPUTS</span></span>

## <span data-ttu-id="fe4b1-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe4b1-125">NOTES</span></span>

## <span data-ttu-id="fe4b1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe4b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="fe4b1-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe4b1-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="fe4b1-128">Nowe — AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe4b1-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="fe4b1-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe4b1-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


