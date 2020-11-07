---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899168"
---
# <span data-ttu-id="42ac0-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="42ac0-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="42ac0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="42ac0-103">Tworzy zapisane zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac0-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ac0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42ac0-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42ac0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42ac0-105">DESCRIPTION</span></span>
<span data-ttu-id="42ac0-106">Polecenie cmdlet **New-AzureStorageTableStoredAccessPolicy** tworzy zapisane zasady dostępu dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac0-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="42ac0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42ac0-107">EXAMPLES</span></span>

### <span data-ttu-id="42ac0-108">Przykład 1: Tworzenie zasad dostępu przechowywanych w tabeli</span><span class="sxs-lookup"><span data-stu-id="42ac0-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="42ac0-109">To polecenie tworzy zasady dostępu o nazwie Policy02 w tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="42ac0-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="42ac0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42ac0-110">PARAMETERS</span></span>

### <span data-ttu-id="42ac0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="42ac0-111">-Context</span></span>
<span data-ttu-id="42ac0-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="42ac0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="42ac0-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="42ac0-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="42ac0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ac0-114">-DefaultProfile</span></span>
<span data-ttu-id="42ac0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42ac0-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="42ac0-116">-ExpiryTime</span></span>
<span data-ttu-id="42ac0-117">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="42ac0-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="42ac0-118">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="42ac0-118">-Permission</span></span>
<span data-ttu-id="42ac0-119">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do tabeli magazynów.</span><span class="sxs-lookup"><span data-stu-id="42ac0-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="42ac0-120">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="42ac0-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="42ac0-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="42ac0-121">-Policy</span></span>
<span data-ttu-id="42ac0-122">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="42ac0-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="42ac0-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="42ac0-123">-StartTime</span></span>
<span data-ttu-id="42ac0-124">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="42ac0-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="42ac0-125">-Table</span><span class="sxs-lookup"><span data-stu-id="42ac0-125">-Table</span></span>
<span data-ttu-id="42ac0-126">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac0-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="42ac0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ac0-127">CommonParameters</span></span>
<span data-ttu-id="42ac0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ac0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ac0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ac0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ac0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42ac0-130">INPUTS</span></span>

### <span data-ttu-id="42ac0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42ac0-131">System.String</span></span>

### <span data-ttu-id="42ac0-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="42ac0-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="42ac0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42ac0-133">OUTPUTS</span></span>

### <span data-ttu-id="42ac0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="42ac0-134">System.String</span></span>

## <span data-ttu-id="42ac0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42ac0-135">NOTES</span></span>

## <span data-ttu-id="42ac0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42ac0-136">RELATED LINKS</span></span>

[<span data-ttu-id="42ac0-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="42ac0-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="42ac0-138">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="42ac0-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="42ac0-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="42ac0-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="42ac0-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="42ac0-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


