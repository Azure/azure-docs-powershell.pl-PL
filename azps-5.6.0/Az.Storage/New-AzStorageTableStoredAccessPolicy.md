---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: cf783e708f4e37de209681e65d19f51ea6aea80b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963521"
---
# <span data-ttu-id="5d770-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5d770-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5d770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d770-102">SYNOPSIS</span></span>
<span data-ttu-id="5d770-103">Tworzy przechowywane zasady dostępu dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d770-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="5d770-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d770-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d770-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d770-105">DESCRIPTION</span></span>
<span data-ttu-id="5d770-106">Polecenie **cmdlet New-AzStorageTableStoredAccessPolicy** tworzy zasady dostępu przechowywanego dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d770-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="5d770-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d770-107">EXAMPLES</span></span>

### <span data-ttu-id="5d770-108">Przykład 1. Tworzenie przechowywanych zasad dostępu w tabeli</span><span class="sxs-lookup"><span data-stu-id="5d770-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="5d770-109">To polecenie tworzy zasady dostępu o nazwie Zasady02 w tabeli magazynu o nazwie Moja tabela.</span><span class="sxs-lookup"><span data-stu-id="5d770-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="5d770-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d770-110">PARAMETERS</span></span>

### <span data-ttu-id="5d770-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5d770-111">-Context</span></span>
<span data-ttu-id="5d770-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d770-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5d770-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d770-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5d770-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d770-114">-DefaultProfile</span></span>
<span data-ttu-id="5d770-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d770-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d770-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5d770-116">-ExpiryTime</span></span>
<span data-ttu-id="5d770-117">Określa czas, w którym przechowywane zasady dostępu stają się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="5d770-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="5d770-118">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="5d770-118">-Permission</span></span>
<span data-ttu-id="5d770-119">Określa uprawnienia w przechowywanych zasadach dostępu do uzyskiwania dostępu do tabeli magazynu.</span><span class="sxs-lookup"><span data-stu-id="5d770-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="5d770-120">Należy pamiętać, że jest to ciąg, taki jak `raud` (w przypadku odczytu, dodawania, aktualizowania i usuwania).</span><span class="sxs-lookup"><span data-stu-id="5d770-120">It is important to note that this is a string, like `raud` (for Read, Add, Update and Delete).</span></span>

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

### <span data-ttu-id="5d770-121">— Zasady</span><span class="sxs-lookup"><span data-stu-id="5d770-121">-Policy</span></span>
<span data-ttu-id="5d770-122">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="5d770-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="5d770-123">— StartTime</span><span class="sxs-lookup"><span data-stu-id="5d770-123">-StartTime</span></span>
<span data-ttu-id="5d770-124">Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="5d770-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="5d770-125">— Tabela</span><span class="sxs-lookup"><span data-stu-id="5d770-125">-Table</span></span>
<span data-ttu-id="5d770-126">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d770-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="5d770-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d770-127">CommonParameters</span></span>
<span data-ttu-id="5d770-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d770-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d770-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d770-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d770-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d770-130">INPUTS</span></span>

### <span data-ttu-id="5d770-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5d770-131">System.String</span></span>

### <span data-ttu-id="5d770-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5d770-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5d770-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d770-133">OUTPUTS</span></span>

### <span data-ttu-id="5d770-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5d770-134">System.String</span></span>

## <span data-ttu-id="5d770-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d770-135">NOTES</span></span>

## <span data-ttu-id="5d770-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d770-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d770-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5d770-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5d770-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5d770-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5d770-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5d770-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5d770-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5d770-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


