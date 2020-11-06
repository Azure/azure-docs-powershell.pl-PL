---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: 60c93d851e173dd8ee8a5f33ff96bb4e2e12299b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547795"
---
# <span data-ttu-id="e6413-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e6413-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="e6413-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6413-102">SYNOPSIS</span></span>
<span data-ttu-id="e6413-103">Generuje token SAS dla obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e6413-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6413-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6413-104">SYNTAX</span></span>

### <span data-ttu-id="e6413-105">BlobNameWithPermission (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6413-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6413-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e6413-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6413-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="e6413-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6413-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e6413-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6413-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e6413-109">DESCRIPTION</span></span>
<span data-ttu-id="e6413-110">Polecenie cmdlet **New-AzureStorageBlobSASToken** generuje token dostępu współużytkowanego (SAS) dla obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e6413-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="e6413-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6413-111">EXAMPLES</span></span>

### <span data-ttu-id="e6413-112">Przykład 1. Generuj token SAS obiektu BLOB z pełnym uprawnieniem obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="e6413-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="e6413-113">W tym przykładzie Wygenerowano token SAS obiektu BLOB z pełnym uprawnieniem obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="e6413-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="e6413-114">Przykład 2: generowanie tokenu SAS obiektu BLOB z czasem życia</span><span class="sxs-lookup"><span data-stu-id="e6413-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="e6413-115">W tym przykładzie Wygenerowano token SAS obiektu BLOB z czasem życia.</span><span class="sxs-lookup"><span data-stu-id="e6413-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="e6413-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6413-116">PARAMETERS</span></span>

### <span data-ttu-id="e6413-117">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="e6413-117">-Blob</span></span>
<span data-ttu-id="e6413-118">Określa nazwę obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="e6413-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e6413-119">-CloudBlob</span></span>
<span data-ttu-id="e6413-120">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="e6413-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="e6413-121">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="e6413-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-122">-Kontener</span><span class="sxs-lookup"><span data-stu-id="e6413-122">-Container</span></span>
<span data-ttu-id="e6413-123">Określa nazwę kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="e6413-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-124">-Context</span><span class="sxs-lookup"><span data-stu-id="e6413-124">-Context</span></span>
<span data-ttu-id="e6413-125">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e6413-125">Specifies the storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6413-126">-DefaultProfile</span></span>
<span data-ttu-id="e6413-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6413-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6413-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e6413-128">-ExpiryTime</span></span>
<span data-ttu-id="e6413-129">Określa, kiedy wygasa udostępniony podpis dostępu.</span><span class="sxs-lookup"><span data-stu-id="e6413-129">Specifies when the shared access signature expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e6413-130">-FullUri</span></span>
<span data-ttu-id="e6413-131">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="e6413-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e6413-132">-IPAddressOrRange</span></span>
<span data-ttu-id="e6413-133">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="e6413-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e6413-134">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="e6413-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="e6413-135">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="e6413-135">-Permission</span></span>
<span data-ttu-id="e6413-136">Określa uprawnienia obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="e6413-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="e6413-137">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="e6413-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-138">-Policy</span><span class="sxs-lookup"><span data-stu-id="e6413-138">-Policy</span></span>
<span data-ttu-id="e6413-139">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e6413-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-140">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e6413-140">-Protocol</span></span>
<span data-ttu-id="e6413-141">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="e6413-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e6413-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6413-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e6413-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e6413-143">HttpsOnly</span></span>
* <span data-ttu-id="e6413-144">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e6413-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e6413-145">-StartTime</span></span>
<span data-ttu-id="e6413-146">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="e6413-146">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6413-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6413-147">CommonParameters</span></span>
<span data-ttu-id="e6413-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6413-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6413-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6413-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6413-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6413-150">INPUTS</span></span>

### <span data-ttu-id="e6413-151">Microsoft. platformy windowsazure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e6413-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e6413-152">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e6413-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e6413-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6413-153">OUTPUTS</span></span>

### <span data-ttu-id="e6413-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e6413-154">System.String</span></span>

## <span data-ttu-id="e6413-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6413-155">NOTES</span></span>

## <span data-ttu-id="e6413-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6413-156">RELATED LINKS</span></span>

[<span data-ttu-id="e6413-157">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e6413-157">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="e6413-158">Nowe — AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e6413-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
