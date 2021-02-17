---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194666"
---
# <span data-ttu-id="589cd-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="589cd-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="589cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="589cd-102">SYNOPSIS</span></span>
<span data-ttu-id="589cd-103">Pobiera wpis w liście ACL pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="589cd-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="589cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="589cd-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="589cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="589cd-105">DESCRIPTION</span></span>
<span data-ttu-id="589cd-106">Polecenie **cmdlet Get-AzDataLakeStoreItemAclEntry** pobiera wpis (ACE) na liście kontroli dostępu (ACL) pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="589cd-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="589cd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="589cd-107">EXAMPLES</span></span>

### <span data-ttu-id="589cd-108">Przykład 1. Uzyskiwanie listy ACL dla folderu</span><span class="sxs-lookup"><span data-stu-id="589cd-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="589cd-109">To polecenie pobiera wartość ACL dla katalogu głównego określonego konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="589cd-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="589cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="589cd-110">PARAMETERS</span></span>

### <span data-ttu-id="589cd-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="589cd-111">-Account</span></span>
<span data-ttu-id="589cd-112">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="589cd-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589cd-113">-DefaultProfile</span></span>
<span data-ttu-id="589cd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="589cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589cd-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="589cd-115">-Path</span></span>
<span data-ttu-id="589cd-116">Określa ścieżkę magazynu usługi Data Lake Store elementu, dla którego to polecenie cmdlet uzyskuje wpis ACE, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="589cd-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589cd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589cd-117">CommonParameters</span></span>
<span data-ttu-id="589cd-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="589cd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589cd-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="589cd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589cd-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="589cd-120">INPUTS</span></span>

### <span data-ttu-id="589cd-121">System.String</span><span class="sxs-lookup"><span data-stu-id="589cd-121">System.String</span></span>

### <span data-ttu-id="589cd-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="589cd-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="589cd-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="589cd-123">OUTPUTS</span></span>

### <span data-ttu-id="589cd-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="589cd-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="589cd-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="589cd-125">NOTES</span></span>

## <span data-ttu-id="589cd-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="589cd-126">RELATED LINKS</span></span>

[<span data-ttu-id="589cd-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="589cd-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="589cd-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="589cd-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


