---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347125"
---
# <span data-ttu-id="1ffd0-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1ffd0-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="1ffd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ffd0-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffd0-103">Pobiera wpis z listy ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ffd0-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1ffd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ffd0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ffd0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ffd0-105">DESCRIPTION</span></span>
<span data-ttu-id="1ffd0-106">Polecenie cmdlet **Get-AzDataLakeStoreItemAclEntry** pobiera wpis (ACE) z listy kontroli dostępu (ACL) do pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ffd0-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1ffd0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ffd0-107">EXAMPLES</span></span>

### <span data-ttu-id="1ffd0-108">Przykład 1. Pobieranie listy ACL dla folderu</span><span class="sxs-lookup"><span data-stu-id="1ffd0-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="1ffd0-109">To polecenie pobiera listę ACL katalogu głównego określonego konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="1ffd0-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="1ffd0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ffd0-110">PARAMETERS</span></span>

### <span data-ttu-id="1ffd0-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="1ffd0-111">-Account</span></span>
<span data-ttu-id="1ffd0-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ffd0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1ffd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffd0-113">-DefaultProfile</span></span>
<span data-ttu-id="1ffd0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ffd0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ffd0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1ffd0-115">-Path</span></span>
<span data-ttu-id="1ffd0-116">Określa ścieżkę do usługi Data Lake Store elementu, dla którego to polecenie cmdlet pobiera wpis ACE, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="1ffd0-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1ffd0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffd0-117">CommonParameters</span></span>
<span data-ttu-id="1ffd0-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ffd0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffd0-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ffd0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffd0-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ffd0-120">INPUTS</span></span>

### <span data-ttu-id="1ffd0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1ffd0-121">System.String</span></span>

### <span data-ttu-id="1ffd0-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1ffd0-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="1ffd0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ffd0-123">OUTPUTS</span></span>

### <span data-ttu-id="1ffd0-124">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="1ffd0-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="1ffd0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ffd0-125">NOTES</span></span>

## <span data-ttu-id="1ffd0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ffd0-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ffd0-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1ffd0-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="1ffd0-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1ffd0-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


