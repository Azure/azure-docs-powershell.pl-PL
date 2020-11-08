---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: 240da78c14b681b334d0793bfc15b2af4d97b5f3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061730"
---
# <span data-ttu-id="f3b12-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b12-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="f3b12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3b12-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b12-103">Dodaje certyfikat do określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f3b12-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="f3b12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3b12-104">SYNTAX</span></span>

### <span data-ttu-id="f3b12-105">Plik (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f3b12-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3b12-106">RawData</span><span class="sxs-lookup"><span data-stu-id="f3b12-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3b12-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f3b12-107">DESCRIPTION</span></span>
<span data-ttu-id="f3b12-108">Polecenie cmdlet **New-AzBatchCertificate** umożliwia dodanie certyfikatu do określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="f3b12-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="f3b12-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3b12-109">EXAMPLES</span></span>

### <span data-ttu-id="f3b12-110">Przykład 1: Dodawanie certyfikatu z pliku</span><span class="sxs-lookup"><span data-stu-id="f3b12-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="f3b12-111">To polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu pliku E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="f3b12-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="f3b12-112">Przykład 2: Dodawanie certyfikatu z danych nieprzetworzonych</span><span class="sxs-lookup"><span data-stu-id="f3b12-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="f3b12-113">Pierwsze polecenie odczytuje dane z pliku o nazwie Moje CERT. pfx do zmiennej $RawData.</span><span class="sxs-lookup"><span data-stu-id="f3b12-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="f3b12-114">Drugie polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu danych pierwotnych przechowywanych w $RawData.</span><span class="sxs-lookup"><span data-stu-id="f3b12-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="f3b12-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3b12-115">PARAMETERS</span></span>

### <span data-ttu-id="f3b12-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f3b12-116">-BatchContext</span></span>
<span data-ttu-id="f3b12-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f3b12-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f3b12-118">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f3b12-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f3b12-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="f3b12-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f3b12-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="f3b12-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f3b12-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f3b12-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f3b12-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b12-122">-DefaultProfile</span></span>
<span data-ttu-id="f3b12-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b12-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3b12-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f3b12-124">-FilePath</span></span>
<span data-ttu-id="f3b12-125">Określa ścieżkę pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f3b12-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="f3b12-126">Plik certyfikatu musi znajdować się w formacie cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="f3b12-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="f3b12-127">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="f3b12-127">-Password</span></span>
<span data-ttu-id="f3b12-128">Określa hasło dostępu do prywatnego klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f3b12-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="f3b12-129">Jeśli określisz certyfikat w formacie PFX, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f3b12-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="f3b12-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="f3b12-130">-RawData</span></span>
<span data-ttu-id="f3b12-131">Określa dane certyfikatu surowego w formacie cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="f3b12-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="f3b12-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b12-132">CommonParameters</span></span>
<span data-ttu-id="f3b12-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b12-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b12-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3b12-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b12-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3b12-135">INPUTS</span></span>

### <span data-ttu-id="f3b12-136">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="f3b12-136">System.Byte[]</span></span>

### <span data-ttu-id="f3b12-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f3b12-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f3b12-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3b12-138">OUTPUTS</span></span>

### <span data-ttu-id="f3b12-139">System. void</span><span class="sxs-lookup"><span data-stu-id="f3b12-139">System.Void</span></span>

## <span data-ttu-id="f3b12-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3b12-140">NOTES</span></span>

## <span data-ttu-id="f3b12-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3b12-141">RELATED LINKS</span></span>

[<span data-ttu-id="f3b12-142">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b12-142">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="f3b12-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f3b12-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f3b12-144">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f3b12-144">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="f3b12-145">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f3b12-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


