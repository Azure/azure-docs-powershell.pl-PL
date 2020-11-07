---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898838"
---
# <span data-ttu-id="19b55-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19b55-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="19b55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19b55-102">SYNOPSIS</span></span>
<span data-ttu-id="19b55-103">Pobiera zasady lub zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19b55-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19b55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19b55-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19b55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19b55-105">DESCRIPTION</span></span>
<span data-ttu-id="19b55-106">Polecenie cmdlet **Get-AzureStorageTableStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dotyczących tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19b55-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="19b55-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19b55-107">EXAMPLES</span></span>

### <span data-ttu-id="19b55-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="19b55-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="19b55-109">To polecenie pobiera zasady dostępu o nazwie Policy50 w tabeli magazynu o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="19b55-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="19b55-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="19b55-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="19b55-111">To polecenie pobiera wszystkie zasady dostępu w tabeli o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="19b55-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="19b55-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19b55-112">PARAMETERS</span></span>

### <span data-ttu-id="19b55-113">-Context</span><span class="sxs-lookup"><span data-stu-id="19b55-113">-Context</span></span>
<span data-ttu-id="19b55-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="19b55-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="19b55-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="19b55-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="19b55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b55-116">-DefaultProfile</span></span>
<span data-ttu-id="19b55-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19b55-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b55-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="19b55-118">-Policy</span></span>
<span data-ttu-id="19b55-119">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="19b55-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19b55-120">-Table</span><span class="sxs-lookup"><span data-stu-id="19b55-120">-Table</span></span>
<span data-ttu-id="19b55-121">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19b55-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="19b55-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b55-122">CommonParameters</span></span>
<span data-ttu-id="19b55-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b55-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b55-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b55-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b55-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19b55-125">INPUTS</span></span>

### <span data-ttu-id="19b55-126">System. String</span><span class="sxs-lookup"><span data-stu-id="19b55-126">System.String</span></span>

### <span data-ttu-id="19b55-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="19b55-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="19b55-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19b55-128">OUTPUTS</span></span>

### <span data-ttu-id="19b55-129">Microsoft. platformy windowsazure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="19b55-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="19b55-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19b55-130">NOTES</span></span>

## <span data-ttu-id="19b55-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19b55-131">RELATED LINKS</span></span>

[<span data-ttu-id="19b55-132">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19b55-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="19b55-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19b55-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="19b55-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19b55-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="19b55-135">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="19b55-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


