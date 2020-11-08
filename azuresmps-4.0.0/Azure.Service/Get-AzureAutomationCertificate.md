---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054629"
---
# <span data-ttu-id="776ab-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="776ab-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="776ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="776ab-102">SYNOPSIS</span></span>

<span data-ttu-id="776ab-103">Pobiera certyfikat usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="776ab-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="776ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="776ab-104">SYNTAX</span></span>

### <span data-ttu-id="776ab-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="776ab-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="776ab-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="776ab-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="776ab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="776ab-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="776ab-108">Polecenie cmdlet **Get-AzureAutomationCertificate** pobiera co najmniej jeden certyfikat usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="776ab-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="776ab-109">Domyślnie wszystkie certyfikaty są zwracane.</span><span class="sxs-lookup"><span data-stu-id="776ab-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="776ab-110">Aby uzyskać określony certyfikat, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="776ab-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="776ab-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="776ab-111">EXAMPLES</span></span>

### <span data-ttu-id="776ab-112">Przykład 1: pobieranie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="776ab-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="776ab-113">To polecenie pobiera wszystkie certyfikaty na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="776ab-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="776ab-114">Przykład 2: uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="776ab-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="776ab-115">To polecenie pobiera certyfikat o nazwie MyUserCertificate.</span><span class="sxs-lookup"><span data-stu-id="776ab-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="776ab-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="776ab-116">PARAMETERS</span></span>

### <span data-ttu-id="776ab-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="776ab-117">-AutomationAccountName</span></span>
<span data-ttu-id="776ab-118">Określa nazwę konta automatyzacji z certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="776ab-118">Specifies the name of the automation account with the certificate.</span></span>

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

### <span data-ttu-id="776ab-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="776ab-119">-Name</span></span>
<span data-ttu-id="776ab-120">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="776ab-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776ab-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="776ab-121">-Profile</span></span>
<span data-ttu-id="776ab-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="776ab-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="776ab-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="776ab-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="776ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776ab-124">CommonParameters</span></span>
<span data-ttu-id="776ab-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="776ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776ab-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="776ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776ab-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="776ab-127">INPUTS</span></span>

## <span data-ttu-id="776ab-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="776ab-128">OUTPUTS</span></span>

### <span data-ttu-id="776ab-129">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="776ab-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="776ab-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="776ab-130">NOTES</span></span>

## <span data-ttu-id="776ab-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="776ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="776ab-132">Nowe — AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="776ab-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="776ab-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="776ab-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="776ab-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="776ab-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


