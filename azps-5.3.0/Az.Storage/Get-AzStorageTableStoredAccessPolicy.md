---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489285"
---
# <span data-ttu-id="3363a-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3363a-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3363a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3363a-102">SYNOPSIS</span></span>
<span data-ttu-id="3363a-103">Pobiera zasady lub zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3363a-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3363a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3363a-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3363a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3363a-105">DESCRIPTION</span></span>
<span data-ttu-id="3363a-106">Polecenie cmdlet **Get-AzStorageTableStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dotyczących tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3363a-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3363a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3363a-107">EXAMPLES</span></span>

### <span data-ttu-id="3363a-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="3363a-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="3363a-109">To polecenie pobiera zasady dostępu o nazwie Policy50 w tabeli magazynu o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="3363a-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="3363a-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="3363a-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="3363a-111">To polecenie pobiera wszystkie zasady dostępu w tabeli o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="3363a-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="3363a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3363a-112">PARAMETERS</span></span>

### <span data-ttu-id="3363a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3363a-113">-Context</span></span>
<span data-ttu-id="3363a-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3363a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3363a-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3363a-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3363a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3363a-116">-DefaultProfile</span></span>
<span data-ttu-id="3363a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3363a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3363a-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="3363a-118">-Policy</span></span>
<span data-ttu-id="3363a-119">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="3363a-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="3363a-120">-Table</span><span class="sxs-lookup"><span data-stu-id="3363a-120">-Table</span></span>
<span data-ttu-id="3363a-121">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3363a-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="3363a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3363a-122">CommonParameters</span></span>
<span data-ttu-id="3363a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3363a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3363a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3363a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3363a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3363a-125">INPUTS</span></span>

### <span data-ttu-id="3363a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3363a-126">System.String</span></span>

### <span data-ttu-id="3363a-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3363a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3363a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3363a-128">OUTPUTS</span></span>

### <span data-ttu-id="3363a-129">Microsoft. platformy windowsazure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="3363a-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="3363a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3363a-130">NOTES</span></span>

## <span data-ttu-id="3363a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3363a-131">RELATED LINKS</span></span>

[<span data-ttu-id="3363a-132">Nowe — AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3363a-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3363a-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3363a-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3363a-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3363a-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3363a-135">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3363a-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


