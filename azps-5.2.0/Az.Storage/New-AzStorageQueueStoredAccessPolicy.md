---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324674"
---
# <span data-ttu-id="aedf7-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aedf7-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="aedf7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aedf7-102">SYNOPSIS</span></span>
<span data-ttu-id="aedf7-103">Tworzy zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aedf7-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="aedf7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aedf7-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aedf7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aedf7-105">DESCRIPTION</span></span>
<span data-ttu-id="aedf7-106">Polecenie cmdlet **New-AzStorageQueueStoredAccessPolicy** tworzy zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aedf7-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="aedf7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aedf7-107">EXAMPLES</span></span>

### <span data-ttu-id="aedf7-108">Przykład 1. Tworzenie zapisanych zasad dostępu w kolejce magazynu</span><span class="sxs-lookup"><span data-stu-id="aedf7-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="aedf7-109">To polecenie tworzy zasady dostępu o nazwie Policy01 w kolejce magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="aedf7-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="aedf7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aedf7-110">PARAMETERS</span></span>

### <span data-ttu-id="aedf7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="aedf7-111">-Context</span></span>
<span data-ttu-id="aedf7-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="aedf7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aedf7-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="aedf7-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aedf7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aedf7-114">-DefaultProfile</span></span>
<span data-ttu-id="aedf7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aedf7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aedf7-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="aedf7-116">-ExpiryTime</span></span>
<span data-ttu-id="aedf7-117">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="aedf7-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="aedf7-118">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="aedf7-118">-Permission</span></span>
<span data-ttu-id="aedf7-119">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="aedf7-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="aedf7-120">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="aedf7-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="aedf7-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="aedf7-121">-Policy</span></span>
<span data-ttu-id="aedf7-122">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="aedf7-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedf7-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="aedf7-123">-Queue</span></span>
<span data-ttu-id="aedf7-124">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aedf7-124">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aedf7-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="aedf7-125">-StartTime</span></span>
<span data-ttu-id="aedf7-126">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="aedf7-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="aedf7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aedf7-127">CommonParameters</span></span>
<span data-ttu-id="aedf7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aedf7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aedf7-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aedf7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aedf7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aedf7-130">INPUTS</span></span>

### <span data-ttu-id="aedf7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aedf7-131">System.String</span></span>

### <span data-ttu-id="aedf7-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="aedf7-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aedf7-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aedf7-133">OUTPUTS</span></span>

### <span data-ttu-id="aedf7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aedf7-134">System.String</span></span>

## <span data-ttu-id="aedf7-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aedf7-135">NOTES</span></span>

## <span data-ttu-id="aedf7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aedf7-136">RELATED LINKS</span></span>

[<span data-ttu-id="aedf7-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aedf7-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="aedf7-138">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aedf7-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="aedf7-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aedf7-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="aedf7-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aedf7-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


