---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 17efee05b4d10ce87d327d8b7de26063bfc0cac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716550"
---
# <span data-ttu-id="69df9-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="69df9-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="69df9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69df9-102">SYNOPSIS</span></span>
<span data-ttu-id="69df9-103">Generuje token SAS dla obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="69df9-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69df9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69df9-104">SYNTAX</span></span>

### <span data-ttu-id="69df9-105">BlobNameWithPermission (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69df9-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="69df9-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="69df9-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="69df9-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="69df9-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="69df9-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="69df9-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="69df9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="69df9-109">DESCRIPTION</span></span>
<span data-ttu-id="69df9-110">Polecenie cmdlet **New-AzureStorageBlobSASToken** generuje token dostępu współużytkowanego (SAS) dla obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="69df9-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="69df9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69df9-111">EXAMPLES</span></span>

### <span data-ttu-id="69df9-112">Przykład 1. Generuj token SAS obiektu BLOB z pełnym uprawnieniem obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="69df9-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="69df9-113">W tym przykładzie Wygenerowano token SAS obiektu BLOB z pełnym uprawnieniem obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="69df9-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="69df9-114">Przykład 2: generowanie tokenu SAS obiektu BLOB z czasem życia</span><span class="sxs-lookup"><span data-stu-id="69df9-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="69df9-115">W tym przykładzie Wygenerowano token SAS obiektu BLOB z czasem życia.</span><span class="sxs-lookup"><span data-stu-id="69df9-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="69df9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69df9-116">PARAMETERS</span></span>

### <span data-ttu-id="69df9-117">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="69df9-117">-Blob</span></span>
<span data-ttu-id="69df9-118">Określa nazwę obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="69df9-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="69df9-119">-CloudBlob</span></span>
<span data-ttu-id="69df9-120">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="69df9-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="69df9-121">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="69df9-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-122">-Kontener</span><span class="sxs-lookup"><span data-stu-id="69df9-122">-Container</span></span>
<span data-ttu-id="69df9-123">Określa nazwę kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="69df9-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-124">-Context</span><span class="sxs-lookup"><span data-stu-id="69df9-124">-Context</span></span>
<span data-ttu-id="69df9-125">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="69df9-125">Specifies the storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="69df9-126">-ExpiryTime</span></span>
<span data-ttu-id="69df9-127">Określa, kiedy wygasa udostępniony podpis dostępu.</span><span class="sxs-lookup"><span data-stu-id="69df9-127">Specifies when the shared access signature expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="69df9-128">-FullUri</span></span>
<span data-ttu-id="69df9-129">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="69df9-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="69df9-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="69df9-130">-IPAddressOrRange</span></span>
<span data-ttu-id="69df9-131">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="69df9-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="69df9-132">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="69df9-132">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-133">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="69df9-133">-Permission</span></span>
<span data-ttu-id="69df9-134">Określa uprawnienia obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="69df9-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="69df9-135">-Policy</span></span>
<span data-ttu-id="69df9-136">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="69df9-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-137">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="69df9-137">-Protocol</span></span>
<span data-ttu-id="69df9-138">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="69df9-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="69df9-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="69df9-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="69df9-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="69df9-140">HttpsOnly</span></span>
* <span data-ttu-id="69df9-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="69df9-141">HttpsOrHttp</span></span>

<span data-ttu-id="69df9-142">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="69df9-142">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="69df9-143">-StartTime</span></span>
<span data-ttu-id="69df9-144">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="69df9-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69df9-145">CommonParameters</span></span>
<span data-ttu-id="69df9-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69df9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69df9-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69df9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69df9-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69df9-148">INPUTS</span></span>

### <span data-ttu-id="69df9-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="69df9-149">IStorageContext</span></span>

<span data-ttu-id="69df9-150">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="69df9-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="69df9-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69df9-151">OUTPUTS</span></span>

### <span data-ttu-id="69df9-152">System. String</span><span class="sxs-lookup"><span data-stu-id="69df9-152">System.String</span></span>

## <span data-ttu-id="69df9-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69df9-153">NOTES</span></span>

## <span data-ttu-id="69df9-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69df9-154">RELATED LINKS</span></span>

[<span data-ttu-id="69df9-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="69df9-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="69df9-156">Nowe — AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="69df9-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)