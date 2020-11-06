---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554165"
---
# <span data-ttu-id="384a8-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="384a8-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="384a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="384a8-102">SYNOPSIS</span></span>
<span data-ttu-id="384a8-103">Dodaje certyfikat do określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="384a8-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="384a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="384a8-104">SYNTAX</span></span>

### <span data-ttu-id="384a8-105">Plik (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="384a8-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="384a8-106">RawData</span><span class="sxs-lookup"><span data-stu-id="384a8-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="384a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="384a8-107">DESCRIPTION</span></span>
<span data-ttu-id="384a8-108">Polecenie cmdlet **New-AzureBatchCertificate** umożliwia dodanie certyfikatu do określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="384a8-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="384a8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="384a8-109">EXAMPLES</span></span>

### <span data-ttu-id="384a8-110">Przykład 1: Dodawanie certyfikatu z pliku</span><span class="sxs-lookup"><span data-stu-id="384a8-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="384a8-111">To polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu pliku E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="384a8-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="384a8-112">Przykład 2: Dodawanie certyfikatu z danych nieprzetworzonych</span><span class="sxs-lookup"><span data-stu-id="384a8-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="384a8-113">Pierwsze polecenie odczytuje dane z pliku o nazwie Moje CERT. pfx do zmiennej $RawData.</span><span class="sxs-lookup"><span data-stu-id="384a8-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="384a8-114">Drugie polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu danych pierwotnych przechowywanych w $RawData.</span><span class="sxs-lookup"><span data-stu-id="384a8-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="384a8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="384a8-115">PARAMETERS</span></span>

### <span data-ttu-id="384a8-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="384a8-116">-BatchContext</span></span>
<span data-ttu-id="384a8-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="384a8-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="384a8-118">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="384a8-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="384a8-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="384a8-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="384a8-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="384a8-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="384a8-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="384a8-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="384a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384a8-122">-DefaultProfile</span></span>
<span data-ttu-id="384a8-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="384a8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="384a8-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="384a8-124">-FilePath</span></span>
<span data-ttu-id="384a8-125">Określa ścieżkę pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="384a8-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="384a8-126">Plik certyfikatu musi znajdować się w formacie cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="384a8-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="384a8-127">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="384a8-127">-Password</span></span>
<span data-ttu-id="384a8-128">Określa hasło dostępu do prywatnego klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="384a8-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="384a8-129">Jeśli określisz certyfikat w formacie PFX, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="384a8-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="384a8-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="384a8-130">-RawData</span></span>
<span data-ttu-id="384a8-131">Określa dane certyfikatu surowego w formacie cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="384a8-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="384a8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384a8-132">CommonParameters</span></span>
<span data-ttu-id="384a8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="384a8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384a8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="384a8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384a8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="384a8-135">INPUTS</span></span>

### <span data-ttu-id="384a8-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="384a8-136">BatchAccountContext</span></span>
<span data-ttu-id="384a8-137">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="384a8-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="384a8-138">Byte []</span><span class="sxs-lookup"><span data-stu-id="384a8-138">Byte[]</span></span>
<span data-ttu-id="384a8-139">Parametr "RawData" akceptuje wartość typu "Byte []" z procesu</span><span class="sxs-lookup"><span data-stu-id="384a8-139">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="384a8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="384a8-140">OUTPUTS</span></span>

## <span data-ttu-id="384a8-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="384a8-141">NOTES</span></span>

## <span data-ttu-id="384a8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="384a8-142">RELATED LINKS</span></span>

[<span data-ttu-id="384a8-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="384a8-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="384a8-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="384a8-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="384a8-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="384a8-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="384a8-146">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="384a8-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


