---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719536"
---
# <span data-ttu-id="ad704-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ad704-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="ad704-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad704-102">SYNOPSIS</span></span>
<span data-ttu-id="ad704-103">Dodaje certyfikat do określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="ad704-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad704-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad704-104">SYNTAX</span></span>

### <span data-ttu-id="ad704-105">Plik (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ad704-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad704-106">RawData</span><span class="sxs-lookup"><span data-stu-id="ad704-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad704-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad704-107">DESCRIPTION</span></span>
<span data-ttu-id="ad704-108">Polecenie cmdlet **New-AzureBatchCertificate** umożliwia dodanie certyfikatu do określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="ad704-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="ad704-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad704-109">EXAMPLES</span></span>

### <span data-ttu-id="ad704-110">Przykład 1: Dodawanie certyfikatu z pliku</span><span class="sxs-lookup"><span data-stu-id="ad704-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="ad704-111">To polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu pliku E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="ad704-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="ad704-112">Przykład 2: Dodawanie certyfikatu z danych nieprzetworzonych</span><span class="sxs-lookup"><span data-stu-id="ad704-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="ad704-113">Pierwsze polecenie odczytuje dane z pliku o nazwie Moje CERT. pfx do zmiennej $RawData.</span><span class="sxs-lookup"><span data-stu-id="ad704-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="ad704-114">Drugie polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu danych pierwotnych przechowywanych w $RawData.</span><span class="sxs-lookup"><span data-stu-id="ad704-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="ad704-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad704-115">PARAMETERS</span></span>

### <span data-ttu-id="ad704-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ad704-116">-BatchContext</span></span>
<span data-ttu-id="ad704-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="ad704-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad704-118">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="ad704-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ad704-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="ad704-119">-FilePath</span></span>
<span data-ttu-id="ad704-120">Określa ścieżkę pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ad704-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="ad704-121">Plik certyfikatu musi znajdować się w formacie cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="ad704-121">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="ad704-122">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="ad704-122">-Password</span></span>
<span data-ttu-id="ad704-123">Określa hasło dostępu do prywatnego klucza certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ad704-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="ad704-124">Jeśli określisz certyfikat w formacie PFX, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ad704-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad704-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="ad704-125">-RawData</span></span>
<span data-ttu-id="ad704-126">Określa dane certyfikatu surowego w formacie cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="ad704-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="ad704-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad704-127">-DefaultProfile</span></span>
<span data-ttu-id="ad704-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad704-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad704-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad704-129">CommonParameters</span></span>
<span data-ttu-id="ad704-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad704-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad704-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad704-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad704-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad704-132">INPUTS</span></span>

### <span data-ttu-id="ad704-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ad704-133">BatchAccountContext</span></span>
<span data-ttu-id="ad704-134">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ad704-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ad704-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="ad704-135">Byte[]</span></span>
<span data-ttu-id="ad704-136">Parametr "RawData" akceptuje wartość typu "Byte []" z procesu</span><span class="sxs-lookup"><span data-stu-id="ad704-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="ad704-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad704-137">OUTPUTS</span></span>

## <span data-ttu-id="ad704-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad704-138">NOTES</span></span>

## <span data-ttu-id="ad704-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad704-139">RELATED LINKS</span></span>

[<span data-ttu-id="ad704-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ad704-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="ad704-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ad704-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ad704-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ad704-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="ad704-143">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ad704-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


