---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f676f644cb69880a0b403a4e656ce9cb435b7c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002385"
---
# <span data-ttu-id="28866-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28866-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="28866-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28866-102">SYNOPSIS</span></span>
<span data-ttu-id="28866-103">Tworzy przechowywane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28866-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="28866-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28866-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28866-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="28866-105">DESCRIPTION</span></span>
<span data-ttu-id="28866-106">Polecenie **cmdlet New-AzStorageQueueStoredAccessPolicy** tworzy zasady dostępu przechowywanego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28866-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="28866-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28866-107">EXAMPLES</span></span>

### <span data-ttu-id="28866-108">Przykład 1. Tworzenie zasad dostępu przechowywanego w kolejce magazynu</span><span class="sxs-lookup"><span data-stu-id="28866-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="28866-109">To polecenie tworzy zasady dostępu o nazwie Zasady01 w kolejce magazynu o nazwie Moje kolejkowanie.</span><span class="sxs-lookup"><span data-stu-id="28866-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="28866-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28866-110">PARAMETERS</span></span>

### <span data-ttu-id="28866-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="28866-111">-Context</span></span>
<span data-ttu-id="28866-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28866-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="28866-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28866-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="28866-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28866-114">-DefaultProfile</span></span>
<span data-ttu-id="28866-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="28866-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28866-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="28866-116">-ExpiryTime</span></span>
<span data-ttu-id="28866-117">Określa czas, w którym przechowywane zasady dostępu stają się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="28866-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="28866-118">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="28866-118">-Permission</span></span>
<span data-ttu-id="28866-119">Określa uprawnienia w zasadach dostępu przechowywanego do uzyskiwania dostępu do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="28866-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="28866-120">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="28866-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="28866-121">— Zasady</span><span class="sxs-lookup"><span data-stu-id="28866-121">-Policy</span></span>
<span data-ttu-id="28866-122">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="28866-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="28866-123">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="28866-123">-Queue</span></span>
<span data-ttu-id="28866-124">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28866-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="28866-125">— StartTime</span><span class="sxs-lookup"><span data-stu-id="28866-125">-StartTime</span></span>
<span data-ttu-id="28866-126">Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="28866-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="28866-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28866-127">CommonParameters</span></span>
<span data-ttu-id="28866-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28866-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28866-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28866-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28866-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28866-130">INPUTS</span></span>

### <span data-ttu-id="28866-131">System.String</span><span class="sxs-lookup"><span data-stu-id="28866-131">System.String</span></span>

### <span data-ttu-id="28866-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="28866-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="28866-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28866-133">OUTPUTS</span></span>

### <span data-ttu-id="28866-134">System.String</span><span class="sxs-lookup"><span data-stu-id="28866-134">System.String</span></span>

## <span data-ttu-id="28866-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28866-135">NOTES</span></span>

## <span data-ttu-id="28866-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28866-136">RELATED LINKS</span></span>

[<span data-ttu-id="28866-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28866-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="28866-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="28866-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="28866-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28866-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="28866-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28866-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


