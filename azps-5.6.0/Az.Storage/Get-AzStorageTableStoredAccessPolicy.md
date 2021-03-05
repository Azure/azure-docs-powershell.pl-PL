---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994785"
---
# <span data-ttu-id="06464-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06464-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="06464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06464-102">SYNOPSIS</span></span>
<span data-ttu-id="06464-103">Pobiera zasady lub zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06464-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="06464-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06464-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06464-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="06464-105">DESCRIPTION</span></span>
<span data-ttu-id="06464-106">Polecenie **cmdlet Get-AzStorageTableStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06464-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="06464-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06464-107">EXAMPLES</span></span>

### <span data-ttu-id="06464-108">Przykład 1. Uzyskiwanie przechowywanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="06464-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="06464-109">To polecenie pobiera zasady dostępu o nazwie Zasady50 w tabeli magazynu o nazwie Tabela02.</span><span class="sxs-lookup"><span data-stu-id="06464-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="06464-110">Przykład 2. Uzyskiwanie wszystkich przechowywanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="06464-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="06464-111">To polecenie pobiera wszystkie zasady dostępu w tabeli o nazwie Tabela02.</span><span class="sxs-lookup"><span data-stu-id="06464-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="06464-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06464-112">PARAMETERS</span></span>

### <span data-ttu-id="06464-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="06464-113">-Context</span></span>
<span data-ttu-id="06464-114">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06464-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="06464-115">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06464-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="06464-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06464-116">-DefaultProfile</span></span>
<span data-ttu-id="06464-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06464-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06464-118">— Zasady</span><span class="sxs-lookup"><span data-stu-id="06464-118">-Policy</span></span>
<span data-ttu-id="06464-119">Określa zasady przechowywanego dostępu, które zawierają uprawnienia do tego tokenu SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="06464-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="06464-120">— Tabela</span><span class="sxs-lookup"><span data-stu-id="06464-120">-Table</span></span>
<span data-ttu-id="06464-121">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06464-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="06464-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06464-122">CommonParameters</span></span>
<span data-ttu-id="06464-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06464-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06464-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06464-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06464-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06464-125">INPUTS</span></span>

### <span data-ttu-id="06464-126">System.String</span><span class="sxs-lookup"><span data-stu-id="06464-126">System.String</span></span>

### <span data-ttu-id="06464-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06464-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="06464-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06464-128">OUTPUTS</span></span>

### <span data-ttu-id="06464-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="06464-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="06464-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06464-130">NOTES</span></span>

## <span data-ttu-id="06464-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06464-131">RELATED LINKS</span></span>

[<span data-ttu-id="06464-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06464-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="06464-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06464-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="06464-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06464-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="06464-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="06464-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


