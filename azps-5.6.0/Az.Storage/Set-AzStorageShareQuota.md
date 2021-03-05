---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 132ad47cd52f258b78ac944342d86979a69abbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007546"
---
# <span data-ttu-id="17222-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="17222-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="17222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17222-102">SYNOPSIS</span></span>
<span data-ttu-id="17222-103">Ustawia pojemność magazynu dla udziału.</span><span class="sxs-lookup"><span data-stu-id="17222-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="17222-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17222-104">SYNTAX</span></span>

### <span data-ttu-id="17222-105">ShareName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="17222-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="17222-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="17222-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="17222-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="17222-107">DESCRIPTION</span></span>
<span data-ttu-id="17222-108">Polecenie **cmdlet Set-AzStorageShareQuota** ustawia pojemność magazynu dla określonego udziału.</span><span class="sxs-lookup"><span data-stu-id="17222-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="17222-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17222-109">EXAMPLES</span></span>

### <span data-ttu-id="17222-110">Przykład 1. Ustawianie pojemności magazynu udziału</span><span class="sxs-lookup"><span data-stu-id="17222-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="17222-111">To polecenie ustawia pojemność magazynowania dla udziału o nazwie ContosoShare01 na 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="17222-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="17222-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17222-112">PARAMETERS</span></span>

### <span data-ttu-id="17222-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="17222-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="17222-114">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="17222-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="17222-115">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="17222-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="17222-116">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="17222-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17222-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="17222-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="17222-118">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="17222-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="17222-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="17222-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="17222-120">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="17222-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="17222-121">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="17222-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="17222-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="17222-122">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17222-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="17222-123">-Context</span></span>
<span data-ttu-id="17222-124">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17222-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="17222-125">Aby uzyskać kontekst przechowywania, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="17222-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17222-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17222-126">-DefaultProfile</span></span>
<span data-ttu-id="17222-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17222-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17222-128">— Przydział</span><span class="sxs-lookup"><span data-stu-id="17222-128">-Quota</span></span>
<span data-ttu-id="17222-129">Określa wartość przydziału w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="17222-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="17222-130">Zobacz ograniczenie przydziału https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits w.</span><span class="sxs-lookup"><span data-stu-id="17222-130">See the quota limitation in https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17222-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="17222-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="17222-132">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="17222-132">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17222-133">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="17222-133">-Share</span></span>
<span data-ttu-id="17222-134">Określa obiekt **CloudFileShare** reprezentujący udział, dla którego to polecenia cmdlet ustawia przydział.</span><span class="sxs-lookup"><span data-stu-id="17222-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="17222-135">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17222-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17222-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="17222-136">-ShareName</span></span>
<span data-ttu-id="17222-137">Określa nazwę udziału plików, dla którego ma być ustawiany przydział.</span><span class="sxs-lookup"><span data-stu-id="17222-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17222-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17222-138">CommonParameters</span></span>
<span data-ttu-id="17222-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17222-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17222-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17222-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17222-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17222-141">INPUTS</span></span>

### <span data-ttu-id="17222-142">System.String</span><span class="sxs-lookup"><span data-stu-id="17222-142">System.String</span></span>

### <span data-ttu-id="17222-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="17222-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="17222-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="17222-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="17222-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17222-145">OUTPUTS</span></span>

### <span data-ttu-id="17222-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="17222-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="17222-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17222-147">NOTES</span></span>

## <span data-ttu-id="17222-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17222-148">RELATED LINKS</span></span>

[<span data-ttu-id="17222-149">Get-AzstorageFileContent</span><span class="sxs-lookup"><span data-stu-id="17222-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="17222-150">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="17222-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="17222-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="17222-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
