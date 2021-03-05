---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: 4ef75210204cddc8de2aa129f0997cb4f12269b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972202"
---
# <span data-ttu-id="ed4e1-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ed4e1-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="ed4e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4e1-103">Dodaje certyfikat do określonego konta usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="ed4e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed4e1-104">SYNTAX</span></span>

### <span data-ttu-id="ed4e1-105">Plik (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed4e1-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed4e1-106">RawData</span><span class="sxs-lookup"><span data-stu-id="ed4e1-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed4e1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed4e1-107">DESCRIPTION</span></span>
<span data-ttu-id="ed4e1-108">Polecenie **cmdlet New-AzBatchCertificate** dodaje certyfikat do określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="ed4e1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed4e1-109">EXAMPLES</span></span>

### <span data-ttu-id="ed4e1-110">Przykład 1. Dodawanie certyfikatu z pliku</span><span class="sxs-lookup"><span data-stu-id="ed4e1-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="ed4e1-111">To polecenie dodaje certyfikat do określonego konta usługi Batch, używając pliku E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="ed4e1-112">Przykład 2. Dodawanie certyfikatu z nieprzetworzonych danych</span><span class="sxs-lookup"><span data-stu-id="ed4e1-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="ed4e1-113">Pierwsze polecenie odczytuje dane z pliku o nazwie MyCert.pfx do zmiennej $RawData pliku.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="ed4e1-114">Drugie polecenie powoduje dodanie certyfikatu do określonego konta usługi Batch przy użyciu nieprzetworzonych danych przechowywanych w $RawData.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="ed4e1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed4e1-115">PARAMETERS</span></span>

### <span data-ttu-id="ed4e1-116">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="ed4e1-116">-BatchContext</span></span>
<span data-ttu-id="ed4e1-117">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ed4e1-118">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ed4e1-119">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ed4e1-120">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ed4e1-121">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4e1-122">-DefaultProfile</span></span>
<span data-ttu-id="ed4e1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4e1-124">- FilePath</span><span class="sxs-lookup"><span data-stu-id="ed4e1-124">-FilePath</span></span>
<span data-ttu-id="ed4e1-125">Określa ścieżkę pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="ed4e1-126">Plik certyfikatu musi mieć format cer lub pfx.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4e1-127">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="ed4e1-127">-Kind</span></span>
<span data-ttu-id="ed4e1-128">Rodzaj certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-128">The kind of certificate to create.</span></span> <span data-ttu-id="ed4e1-129">Jeśli nie zostanie to określone, przyjmuje się, że wszystkie certyfikaty bez hasła są certyfikatem CER, a wszystkie certyfikaty z hasłem są pfx.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4e1-130">— Hasło</span><span class="sxs-lookup"><span data-stu-id="ed4e1-130">-Password</span></span>
<span data-ttu-id="ed4e1-131">Określa hasło dostępu do klucza prywatnego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="ed4e1-132">Ten parametr należy określić, jeśli zostanie określony certyfikat w formacie pfx.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4e1-133">- RawData</span><span class="sxs-lookup"><span data-stu-id="ed4e1-133">-RawData</span></span>
<span data-ttu-id="ed4e1-134">Określa nieprzetworzone dane certyfikatu w formacie cer lub pfx.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4e1-135">CommonParameters</span></span>
<span data-ttu-id="ed4e1-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4e1-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed4e1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4e1-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed4e1-138">INPUTS</span></span>

### <span data-ttu-id="ed4e1-139">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="ed4e1-139">System.Byte[]</span></span>

### <span data-ttu-id="ed4e1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ed4e1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ed4e1-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed4e1-141">OUTPUTS</span></span>

### <span data-ttu-id="ed4e1-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="ed4e1-142">System.Void</span></span>

## <span data-ttu-id="ed4e1-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed4e1-143">NOTES</span></span>

## <span data-ttu-id="ed4e1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed4e1-144">RELATED LINKS</span></span>

[<span data-ttu-id="ed4e1-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ed4e1-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="ed4e1-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed4e1-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ed4e1-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ed4e1-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="ed4e1-148">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed4e1-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
