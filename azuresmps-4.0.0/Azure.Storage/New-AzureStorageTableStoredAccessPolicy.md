---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523022"
---
# <span data-ttu-id="2af2a-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2af2a-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="2af2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2af2a-102">SYNOPSIS</span></span>
<span data-ttu-id="2af2a-103">Tworzy zapisane zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2af2a-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2af2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2af2a-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="2af2a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2af2a-105">DESCRIPTION</span></span>
<span data-ttu-id="2af2a-106">Polecenie cmdlet **New-AzureStorageTableStoredAccessPolicy** tworzy zapisane zasady dostępu dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2af2a-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2af2a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2af2a-107">EXAMPLES</span></span>

### <span data-ttu-id="2af2a-108">Przykład 1: Tworzenie zasad dostępu przechowywanych w tabeli</span><span class="sxs-lookup"><span data-stu-id="2af2a-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="2af2a-109">To polecenie tworzy zasady dostępu o nazwie Policy02 w tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="2af2a-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="2af2a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2af2a-110">PARAMETERS</span></span>

### <span data-ttu-id="2af2a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2af2a-111">-Context</span></span>
<span data-ttu-id="2af2a-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2af2a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2af2a-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2af2a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2af2a-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2af2a-114">-ExpiryTime</span></span>
<span data-ttu-id="2af2a-115">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="2af2a-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="2af2a-116">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="2af2a-116">-Permission</span></span>
<span data-ttu-id="2af2a-117">Określa poziom dostępu publicznego do tej tabeli magazynu.</span><span class="sxs-lookup"><span data-stu-id="2af2a-117">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="2af2a-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="2af2a-118">-Policy</span></span>
<span data-ttu-id="2af2a-119">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="2af2a-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="2af2a-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2af2a-120">-StartTime</span></span>
<span data-ttu-id="2af2a-121">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="2af2a-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="2af2a-122">-Table</span><span class="sxs-lookup"><span data-stu-id="2af2a-122">-Table</span></span>
<span data-ttu-id="2af2a-123">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2af2a-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="2af2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af2a-124">CommonParameters</span></span>
<span data-ttu-id="2af2a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2af2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af2a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2af2a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af2a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2af2a-127">INPUTS</span></span>

## <span data-ttu-id="2af2a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2af2a-128">OUTPUTS</span></span>

## <span data-ttu-id="2af2a-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2af2a-129">NOTES</span></span>

## <span data-ttu-id="2af2a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2af2a-130">RELATED LINKS</span></span>

[<span data-ttu-id="2af2a-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2af2a-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2af2a-132">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2af2a-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2af2a-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2af2a-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2af2a-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2af2a-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


