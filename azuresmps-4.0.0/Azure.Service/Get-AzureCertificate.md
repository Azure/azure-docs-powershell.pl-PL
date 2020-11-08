---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055322"
---
# <span data-ttu-id="1c59f-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59f-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="1c59f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c59f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c59f-103">Pobiera obiekt Certificate z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c59f-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="1c59f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c59f-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c59f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c59f-105">DESCRIPTION</span></span>
<span data-ttu-id="1c59f-106">Polecenie cmdlet **Get-AzureCertificate** pobiera obiekt Certificate z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c59f-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="1c59f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c59f-107">EXAMPLES</span></span>

### <span data-ttu-id="1c59f-108">Przykład 1: uzyskiwanie certyfikatów z usługi</span><span class="sxs-lookup"><span data-stu-id="1c59f-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="1c59f-109">To polecenie pobiera obiekty Certificates z usługi o nazwie ContosoService, a następnie zapisuje je w zmiennej $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="1c59f-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="1c59f-110">Przykład 2: uzyskiwanie certyfikatu z usługi</span><span class="sxs-lookup"><span data-stu-id="1c59f-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="1c59f-111">To polecenie pobiera obiekt Certificate zidentyfikowany przez określony odcisk palca z usługi o nazwie ContosoService, a następnie zapisuje go w zmiennej $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="1c59f-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="1c59f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c59f-112">PARAMETERS</span></span>

### <span data-ttu-id="1c59f-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1c59f-113">-InformationAction</span></span>
<span data-ttu-id="1c59f-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="1c59f-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1c59f-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1c59f-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c59f-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="1c59f-116">Continue</span></span>
- <span data-ttu-id="1c59f-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="1c59f-117">Ignore</span></span>
- <span data-ttu-id="1c59f-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="1c59f-118">Inquire</span></span>
- <span data-ttu-id="1c59f-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1c59f-119">SilentlyContinue</span></span>
- <span data-ttu-id="1c59f-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="1c59f-120">Stop</span></span>
- <span data-ttu-id="1c59f-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="1c59f-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c59f-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1c59f-122">-InformationVariable</span></span>
<span data-ttu-id="1c59f-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="1c59f-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c59f-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="1c59f-124">-Profile</span></span>
<span data-ttu-id="1c59f-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c59f-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c59f-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1c59f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c59f-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1c59f-127">-ServiceName</span></span>
<span data-ttu-id="1c59f-128">Określa nazwę usługi platformy Azure, z której to polecenie cmdlet pobiera certyfikat.</span><span class="sxs-lookup"><span data-stu-id="1c59f-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c59f-129">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="1c59f-129">-Thumbprint</span></span>
<span data-ttu-id="1c59f-130">Określa odcisk palca certyfikatu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c59f-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c59f-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1c59f-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="1c59f-132">Określa algorytm używany do tworzenia odcisku palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1c59f-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c59f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c59f-133">CommonParameters</span></span>
<span data-ttu-id="1c59f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c59f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c59f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c59f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c59f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c59f-136">INPUTS</span></span>

## <span data-ttu-id="1c59f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c59f-137">OUTPUTS</span></span>

### <span data-ttu-id="1c59f-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="1c59f-138">CertificateContext</span></span>

## <span data-ttu-id="1c59f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c59f-139">NOTES</span></span>

## <span data-ttu-id="1c59f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c59f-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c59f-141">Dodaj-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59f-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="1c59f-142">Nowe — AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="1c59f-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="1c59f-143">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="1c59f-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


