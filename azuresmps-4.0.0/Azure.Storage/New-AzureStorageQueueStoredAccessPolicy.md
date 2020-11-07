---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710732"
---
# <span data-ttu-id="3be52-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3be52-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3be52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3be52-102">SYNOPSIS</span></span>
<span data-ttu-id="3be52-103">Tworzy zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3be52-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3be52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3be52-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="3be52-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3be52-105">DESCRIPTION</span></span>
<span data-ttu-id="3be52-106">Polecenie cmdlet **New-AzureStorageQueueStoredAccessPolicy** tworzy zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3be52-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3be52-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3be52-107">EXAMPLES</span></span>

### <span data-ttu-id="3be52-108">Przykład 1. Tworzenie zapisanych zasad dostępu w kolejce magazynu</span><span class="sxs-lookup"><span data-stu-id="3be52-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="3be52-109">To polecenie tworzy zasady dostępu o nazwie Policy01 w kolejce magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="3be52-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="3be52-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3be52-110">PARAMETERS</span></span>

### <span data-ttu-id="3be52-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3be52-111">-Context</span></span>
<span data-ttu-id="3be52-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3be52-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3be52-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3be52-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3be52-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3be52-114">-ExpiryTime</span></span>
<span data-ttu-id="3be52-115">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="3be52-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3be52-116">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="3be52-116">-Permission</span></span>
<span data-ttu-id="3be52-117">Określa poziom dostępu publicznego do tej kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="3be52-117">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="3be52-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="3be52-118">-Policy</span></span>
<span data-ttu-id="3be52-119">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="3be52-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be52-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="3be52-120">-Queue</span></span>
<span data-ttu-id="3be52-121">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3be52-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be52-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3be52-122">-StartTime</span></span>
<span data-ttu-id="3be52-123">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="3be52-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3be52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be52-124">CommonParameters</span></span>
<span data-ttu-id="3be52-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be52-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be52-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3be52-127">INPUTS</span></span>

## <span data-ttu-id="3be52-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3be52-128">OUTPUTS</span></span>

## <span data-ttu-id="3be52-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3be52-129">NOTES</span></span>

## <span data-ttu-id="3be52-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3be52-130">RELATED LINKS</span></span>

[<span data-ttu-id="3be52-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3be52-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3be52-132">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3be52-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3be52-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3be52-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3be52-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3be52-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


