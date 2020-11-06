---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 8473cc65ec6afffb9433159d848d9e7b8629a351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548712"
---
# <span data-ttu-id="33bdb-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33bdb-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="33bdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="33bdb-103">Pobiera wpis z listy ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="33bdb-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33bdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33bdb-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33bdb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33bdb-105">DESCRIPTION</span></span>
<span data-ttu-id="33bdb-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemAclEntry** pobiera wpis (ACE) z listy kontroli dostępu (ACL) do pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="33bdb-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="33bdb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33bdb-107">EXAMPLES</span></span>

### <span data-ttu-id="33bdb-108">Przykład 1. Pobieranie listy ACL dla folderu</span><span class="sxs-lookup"><span data-stu-id="33bdb-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="33bdb-109">To polecenie pobiera listę ACL katalogu głównego określonego konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="33bdb-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="33bdb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33bdb-110">PARAMETERS</span></span>

### <span data-ttu-id="33bdb-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="33bdb-111">-Account</span></span>
<span data-ttu-id="33bdb-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="33bdb-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="33bdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bdb-113">-DefaultProfile</span></span>
<span data-ttu-id="33bdb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33bdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33bdb-115">-Path</span><span class="sxs-lookup"><span data-stu-id="33bdb-115">-Path</span></span>
<span data-ttu-id="33bdb-116">Określa ścieżkę do usługi Data Lake Store elementu, dla którego to polecenie cmdlet pobiera wpis ACE, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="33bdb-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="33bdb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bdb-117">CommonParameters</span></span>
<span data-ttu-id="33bdb-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33bdb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bdb-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33bdb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bdb-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33bdb-120">INPUTS</span></span>

### <span data-ttu-id="33bdb-121">System. String</span><span class="sxs-lookup"><span data-stu-id="33bdb-121">System.String</span></span>

### <span data-ttu-id="33bdb-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="33bdb-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="33bdb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33bdb-123">OUTPUTS</span></span>

### <span data-ttu-id="33bdb-124">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="33bdb-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="33bdb-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33bdb-125">NOTES</span></span>

## <span data-ttu-id="33bdb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33bdb-126">RELATED LINKS</span></span>

[<span data-ttu-id="33bdb-127">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33bdb-127">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="33bdb-128">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33bdb-128">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


