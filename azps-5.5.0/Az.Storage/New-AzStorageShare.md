---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 4fa89a13f9b4124232d9459d7d3eff54a6f55a5c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183186"
---
# <span data-ttu-id="c0e74-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c0e74-101">New-AzStorageShare</span></span>

## <span data-ttu-id="c0e74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0e74-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e74-103">Tworzy udział plików.</span><span class="sxs-lookup"><span data-stu-id="c0e74-103">Creates a file share.</span></span>

## <span data-ttu-id="c0e74-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0e74-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0e74-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0e74-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e74-106">Polecenie **cmdlet New-AzStorageShare** tworzy udział plików.</span><span class="sxs-lookup"><span data-stu-id="c0e74-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="c0e74-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0e74-107">EXAMPLES</span></span>

### <span data-ttu-id="c0e74-108">Przykład 1. Tworzenie udziału plików</span><span class="sxs-lookup"><span data-stu-id="c0e74-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="c0e74-109">To polecenie tworzy udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c0e74-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="c0e74-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0e74-110">PARAMETERS</span></span>

### <span data-ttu-id="c0e74-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0e74-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c0e74-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c0e74-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c0e74-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="c0e74-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c0e74-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="c0e74-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c0e74-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c0e74-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c0e74-116">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c0e74-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c0e74-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c0e74-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c0e74-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="c0e74-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c0e74-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c0e74-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c0e74-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c0e74-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c0e74-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="c0e74-121">-Context</span></span>
<span data-ttu-id="c0e74-122">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e74-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c0e74-123">Aby uzyskać kontekst magazynowania, użyj polecenia cmdlet [New-azStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="c0e74-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c0e74-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e74-124">-DefaultProfile</span></span>
<span data-ttu-id="c0e74-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e74-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0e74-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0e74-126">-Name</span></span>
<span data-ttu-id="c0e74-127">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="c0e74-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="c0e74-128">To polecenie cmdlet tworzy udział plików, który ma nazwę podaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c0e74-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e74-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0e74-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c0e74-130">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="c0e74-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c0e74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e74-131">CommonParameters</span></span>
<span data-ttu-id="c0e74-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e74-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e74-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e74-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0e74-134">INPUTS</span></span>

### <span data-ttu-id="c0e74-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c0e74-135">System.String</span></span>

### <span data-ttu-id="c0e74-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0e74-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c0e74-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0e74-137">OUTPUTS</span></span>

### <span data-ttu-id="c0e74-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="c0e74-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="c0e74-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0e74-139">NOTES</span></span>

## <span data-ttu-id="c0e74-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0e74-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0e74-141">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="c0e74-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c0e74-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0e74-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c0e74-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c0e74-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
