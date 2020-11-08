---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055133"
---
# <span data-ttu-id="dbbac-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="dbbac-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="dbbac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbbac-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbac-103">Usuwa certyfikat z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dbbac-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="dbbac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbbac-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbbac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dbbac-105">DESCRIPTION</span></span>
<span data-ttu-id="dbbac-106">Polecenie cmdlet **Remove-AzureCertificate** usuwa certyfikat z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dbbac-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="dbbac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbbac-107">EXAMPLES</span></span>

### <span data-ttu-id="dbbac-108">Przykład 1: Usuwanie certyfikatu z usługi</span><span class="sxs-lookup"><span data-stu-id="dbbac-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="dbbac-109">To polecenie umożliwia usunięcie obiektu certyfikatu z określonym odciskiem palca z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="dbbac-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="dbbac-110">Przykład 2: Usuwanie wszystkich certyfikatów z usługi</span><span class="sxs-lookup"><span data-stu-id="dbbac-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="dbbac-111">To polecenie pobiera wszystkie certyfikaty z usługi o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="dbbac-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="dbbac-112">Polecenie przekazuje poszczególne certyfikaty do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="dbbac-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dbbac-113">Polecenie cmdlet powoduje usunięcie każdego certyfikatu z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="dbbac-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="dbbac-114">Przykład 3: Usuwanie wszystkich certyfikatów z usługi, która używa konkretnego algorytmu odcisku palca</span><span class="sxs-lookup"><span data-stu-id="dbbac-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="dbbac-115">To polecenie pobiera wszystkie certyfikaty z usługi o nazwie ContosoService, które używają algorytmu odcisku palca SHA1.</span><span class="sxs-lookup"><span data-stu-id="dbbac-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="dbbac-116">Polecenie przekazuje poszczególne certyfikaty do bieżącego polecenia cmdlet, które usuwa każdy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="dbbac-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="dbbac-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbbac-117">PARAMETERS</span></span>

### <span data-ttu-id="dbbac-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dbbac-118">-InformationAction</span></span>
<span data-ttu-id="dbbac-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="dbbac-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dbbac-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dbbac-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbbac-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="dbbac-121">Continue</span></span>
- <span data-ttu-id="dbbac-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="dbbac-122">Ignore</span></span>
- <span data-ttu-id="dbbac-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="dbbac-123">Inquire</span></span>
- <span data-ttu-id="dbbac-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dbbac-124">SilentlyContinue</span></span>
- <span data-ttu-id="dbbac-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="dbbac-125">Stop</span></span>
- <span data-ttu-id="dbbac-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="dbbac-126">Suspend</span></span>

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

### <span data-ttu-id="dbbac-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dbbac-127">-InformationVariable</span></span>
<span data-ttu-id="dbbac-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="dbbac-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dbbac-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="dbbac-129">-Profile</span></span>
<span data-ttu-id="dbbac-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbbac-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dbbac-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="dbbac-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dbbac-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dbbac-132">-ServiceName</span></span>
<span data-ttu-id="dbbac-133">Określa nazwę usługi platformy Azure, z której to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="dbbac-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="dbbac-134">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="dbbac-134">-Thumbprint</span></span>
<span data-ttu-id="dbbac-135">Określa odcisk palca certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="dbbac-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbac-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="dbbac-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="dbbac-137">Określa algorytm używany do tworzenia odcisku palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="dbbac-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbac-138">CommonParameters</span></span>
<span data-ttu-id="dbbac-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbbac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbac-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbbac-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbac-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbbac-141">INPUTS</span></span>

## <span data-ttu-id="dbbac-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbbac-142">OUTPUTS</span></span>

### <span data-ttu-id="dbbac-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="dbbac-143">ManagementOperationContext</span></span>

## <span data-ttu-id="dbbac-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbbac-144">NOTES</span></span>

## <span data-ttu-id="dbbac-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbbac-145">RELATED LINKS</span></span>

[<span data-ttu-id="dbbac-146">Dodaj-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="dbbac-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="dbbac-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="dbbac-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="dbbac-148">Nowe — AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="dbbac-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


