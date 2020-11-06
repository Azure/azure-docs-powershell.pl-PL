---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 163c6ba0841b19edc76421259b1cd9cc8411e35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545867"
---
# <span data-ttu-id="34392-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34392-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="34392-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34392-102">SYNOPSIS</span></span>
<span data-ttu-id="34392-103">Tworzy zapisane zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34392-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34392-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34392-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="34392-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34392-105">DESCRIPTION</span></span>
<span data-ttu-id="34392-106">Polecenie cmdlet **New-AzureStorageTableStoredAccessPolicy** tworzy zapisane zasady dostępu dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34392-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="34392-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34392-107">EXAMPLES</span></span>

### <span data-ttu-id="34392-108">Przykład 1: Tworzenie zasad dostępu przechowywanych w tabeli</span><span class="sxs-lookup"><span data-stu-id="34392-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="34392-109">To polecenie tworzy zasady dostępu o nazwie Policy02 w tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="34392-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="34392-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34392-110">PARAMETERS</span></span>

### <span data-ttu-id="34392-111">-Context</span><span class="sxs-lookup"><span data-stu-id="34392-111">-Context</span></span>
<span data-ttu-id="34392-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="34392-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="34392-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="34392-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="34392-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="34392-114">-ExpiryTime</span></span>
<span data-ttu-id="34392-115">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="34392-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="34392-116">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="34392-116">-Permission</span></span>
<span data-ttu-id="34392-117">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do tabeli magazynów.</span><span class="sxs-lookup"><span data-stu-id="34392-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="34392-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="34392-118">-Policy</span></span>
<span data-ttu-id="34392-119">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="34392-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="34392-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="34392-120">-StartTime</span></span>
<span data-ttu-id="34392-121">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="34392-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="34392-122">-Table</span><span class="sxs-lookup"><span data-stu-id="34392-122">-Table</span></span>
<span data-ttu-id="34392-123">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34392-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="34392-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34392-124">CommonParameters</span></span>
<span data-ttu-id="34392-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34392-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34392-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34392-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34392-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34392-127">INPUTS</span></span>

### <span data-ttu-id="34392-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34392-128">IStorageContext</span></span>

<span data-ttu-id="34392-129">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="34392-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="34392-130">Ciąg</span><span class="sxs-lookup"><span data-stu-id="34392-130">String</span></span>

<span data-ttu-id="34392-131">Parametr "Tabela" przyjmuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="34392-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="34392-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34392-132">OUTPUTS</span></span>

### <span data-ttu-id="34392-133">System. String</span><span class="sxs-lookup"><span data-stu-id="34392-133">System.String</span></span>

## <span data-ttu-id="34392-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34392-134">NOTES</span></span>

## <span data-ttu-id="34392-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34392-135">RELATED LINKS</span></span>

[<span data-ttu-id="34392-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34392-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="34392-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="34392-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="34392-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34392-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="34392-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34392-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


