---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055459"
---
# <span data-ttu-id="37e70-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="37e70-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="37e70-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37e70-102">SYNOPSIS</span></span>

<span data-ttu-id="37e70-103">Usuwa certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="37e70-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="37e70-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37e70-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37e70-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37e70-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="37e70-106">Polecenie cmdlet **Remove-AzureAutomationAccount** usuwa certyfikat z usługi automatyzacji Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37e70-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="37e70-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37e70-107">EXAMPLES</span></span>

### <span data-ttu-id="37e70-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="37e70-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="37e70-109">To polecenie usuwa certyfikat o nazwie Cert01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="37e70-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="37e70-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37e70-110">PARAMETERS</span></span>

### <span data-ttu-id="37e70-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37e70-111">-AutomationAccountName</span></span>
<span data-ttu-id="37e70-112">Określa nazwę konta automatyzacji z certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="37e70-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="37e70-113">-Force</span><span class="sxs-lookup"><span data-stu-id="37e70-113">-Force</span></span>
<span data-ttu-id="37e70-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="37e70-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37e70-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37e70-115">-Name</span></span>
<span data-ttu-id="37e70-116">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="37e70-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="37e70-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="37e70-117">-Profile</span></span>
<span data-ttu-id="37e70-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e70-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37e70-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="37e70-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37e70-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e70-120">CommonParameters</span></span>
<span data-ttu-id="37e70-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e70-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e70-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e70-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e70-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37e70-123">INPUTS</span></span>

## <span data-ttu-id="37e70-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37e70-124">OUTPUTS</span></span>

## <span data-ttu-id="37e70-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37e70-125">NOTES</span></span>

## <span data-ttu-id="37e70-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37e70-126">RELATED LINKS</span></span>

[<span data-ttu-id="37e70-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="37e70-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="37e70-128">Nowe — AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="37e70-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="37e70-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="37e70-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


