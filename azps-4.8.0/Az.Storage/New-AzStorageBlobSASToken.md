---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222761"
---
# <span data-ttu-id="96019-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="96019-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="96019-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96019-102">SYNOPSIS</span></span>
<span data-ttu-id="96019-103">Generuje token SAS dla obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="96019-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="96019-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96019-104">SYNTAX</span></span>

### <span data-ttu-id="96019-105">BlobNameWithPermission (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96019-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96019-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="96019-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96019-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="96019-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96019-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="96019-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96019-109">Opis</span><span class="sxs-lookup"><span data-stu-id="96019-109">DESCRIPTION</span></span>
<span data-ttu-id="96019-110">Polecenie cmdlet **New-AzStorageBlobSASToken** generuje token dostępu współużytkowanego (SAS) dla obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="96019-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="96019-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96019-111">EXAMPLES</span></span>

### <span data-ttu-id="96019-112">Przykład 1. Generuj token SAS obiektu BLOB z pełnym uprawnieniem obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="96019-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="96019-113">W tym przykładzie Wygenerowano token SAS obiektu BLOB z pełnym uprawnieniem obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="96019-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="96019-114">Przykład 2: generowanie tokenu SAS obiektu BLOB z czasem życia</span><span class="sxs-lookup"><span data-stu-id="96019-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="96019-115">W tym przykładzie Wygenerowano token SAS obiektu BLOB z czasem życia.</span><span class="sxs-lookup"><span data-stu-id="96019-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="96019-116">Przykład 3: generowanie tokenu SAS tożsamości użytkownika z kontekstem magazynu na podstawie uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="96019-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="96019-117">W tym przykładzie Wygenerowano token SAS obiektu BLOB tożsamości użytkownika z kontekstem magazynu na podstawie uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="96019-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="96019-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96019-118">PARAMETERS</span></span>

### <span data-ttu-id="96019-119">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="96019-119">-Blob</span></span>
<span data-ttu-id="96019-120">Określa nazwę obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="96019-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="96019-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="96019-121">-BlobBaseClient</span></span>
<span data-ttu-id="96019-122">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="96019-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96019-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="96019-123">-CloudBlob</span></span>
<span data-ttu-id="96019-124">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="96019-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="96019-125">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="96019-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96019-126">-Kontener</span><span class="sxs-lookup"><span data-stu-id="96019-126">-Container</span></span>
<span data-ttu-id="96019-127">Określa nazwę kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="96019-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="96019-128">-Context</span><span class="sxs-lookup"><span data-stu-id="96019-128">-Context</span></span>
<span data-ttu-id="96019-129">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="96019-129">Specifies the storage context.</span></span>
<span data-ttu-id="96019-130">Gdy kontekst magazynu jest oparty na uwierzytelnianiu OAuth, zostanie wygenerowany token SAS obiektu BLOB tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="96019-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="96019-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96019-131">-DefaultProfile</span></span>
<span data-ttu-id="96019-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96019-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96019-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="96019-133">-ExpiryTime</span></span>
<span data-ttu-id="96019-134">Określa, kiedy wygasa udostępniony podpis dostępu.</span><span class="sxs-lookup"><span data-stu-id="96019-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="96019-135">Gdy kontekst magazynu jest oparty na uwierzytelnianiu OAuth, czas wygaśnięcia musi wynosić w ciągu 7 dni od bieżącego czasu i nie może być wcześniejszy niż bieżący czas.</span><span class="sxs-lookup"><span data-stu-id="96019-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="96019-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="96019-136">-FullUri</span></span>
<span data-ttu-id="96019-137">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="96019-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="96019-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="96019-138">-IPAddressOrRange</span></span>
<span data-ttu-id="96019-139">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="96019-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="96019-140">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="96019-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="96019-141">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="96019-141">-Permission</span></span>
<span data-ttu-id="96019-142">Określa uprawnienia obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="96019-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="96019-143">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="96019-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="96019-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="96019-144">-Policy</span></span>
<span data-ttu-id="96019-145">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="96019-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="96019-146">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="96019-146">-Protocol</span></span>
<span data-ttu-id="96019-147">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="96019-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="96019-148">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="96019-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="96019-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="96019-149">HttpsOnly</span></span>
* <span data-ttu-id="96019-150">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="96019-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96019-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="96019-151">-StartTime</span></span>
<span data-ttu-id="96019-152">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="96019-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="96019-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96019-153">-Confirm</span></span>
<span data-ttu-id="96019-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96019-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96019-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96019-155">-WhatIf</span></span>
<span data-ttu-id="96019-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96019-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96019-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96019-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96019-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96019-158">CommonParameters</span></span>
<span data-ttu-id="96019-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96019-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96019-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96019-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96019-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96019-161">INPUTS</span></span>

### <span data-ttu-id="96019-162">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="96019-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="96019-163">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96019-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="96019-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96019-164">OUTPUTS</span></span>

### <span data-ttu-id="96019-165">System. String</span><span class="sxs-lookup"><span data-stu-id="96019-165">System.String</span></span>

## <span data-ttu-id="96019-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96019-166">NOTES</span></span>

## <span data-ttu-id="96019-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96019-167">RELATED LINKS</span></span>

[<span data-ttu-id="96019-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="96019-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="96019-169">Nowe — AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="96019-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
