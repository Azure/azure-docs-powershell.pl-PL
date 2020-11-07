---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: e2e1f8952e0b785c5856585ad3e3371074194afd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888138"
---
# <span data-ttu-id="cab22-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cab22-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="cab22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cab22-102">SYNOPSIS</span></span>
<span data-ttu-id="cab22-103">Tworzy zapisane zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cab22-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="cab22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cab22-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab22-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cab22-105">DESCRIPTION</span></span>
<span data-ttu-id="cab22-106">Polecenie cmdlet **New-AzStorageTableStoredAccessPolicy** tworzy zapisane zasady dostępu dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cab22-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="cab22-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cab22-107">EXAMPLES</span></span>

### <span data-ttu-id="cab22-108">Przykład 1: Tworzenie zasad dostępu przechowywanych w tabeli</span><span class="sxs-lookup"><span data-stu-id="cab22-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="cab22-109">To polecenie tworzy zasady dostępu o nazwie Policy02 w tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="cab22-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="cab22-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cab22-110">PARAMETERS</span></span>

### <span data-ttu-id="cab22-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cab22-111">-Context</span></span>
<span data-ttu-id="cab22-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="cab22-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cab22-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cab22-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cab22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab22-114">-DefaultProfile</span></span>
<span data-ttu-id="cab22-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cab22-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab22-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cab22-116">-ExpiryTime</span></span>
<span data-ttu-id="cab22-117">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="cab22-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="cab22-118">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="cab22-118">-Permission</span></span>
<span data-ttu-id="cab22-119">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do tabeli magazynów.</span><span class="sxs-lookup"><span data-stu-id="cab22-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="cab22-120">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="cab22-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="cab22-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="cab22-121">-Policy</span></span>
<span data-ttu-id="cab22-122">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="cab22-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="cab22-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cab22-123">-StartTime</span></span>
<span data-ttu-id="cab22-124">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="cab22-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="cab22-125">-Table</span><span class="sxs-lookup"><span data-stu-id="cab22-125">-Table</span></span>
<span data-ttu-id="cab22-126">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cab22-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="cab22-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab22-127">CommonParameters</span></span>
<span data-ttu-id="cab22-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab22-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab22-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab22-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab22-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cab22-130">INPUTS</span></span>

### <span data-ttu-id="cab22-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cab22-131">System.String</span></span>

### <span data-ttu-id="cab22-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cab22-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cab22-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cab22-133">OUTPUTS</span></span>

### <span data-ttu-id="cab22-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cab22-134">System.String</span></span>

## <span data-ttu-id="cab22-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cab22-135">NOTES</span></span>

## <span data-ttu-id="cab22-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cab22-136">RELATED LINKS</span></span>

[<span data-ttu-id="cab22-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cab22-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="cab22-138">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cab22-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="cab22-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cab22-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="cab22-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cab22-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


