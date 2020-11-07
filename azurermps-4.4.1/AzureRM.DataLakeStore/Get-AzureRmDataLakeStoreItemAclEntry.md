---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718223"
---
# <span data-ttu-id="2ee7d-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2ee7d-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="2ee7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ee7d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee7d-103">Pobiera wpis z listy ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2ee7d-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ee7d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ee7d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee7d-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemAclEntry** pobiera wpis (ACE) z listy kontroli dostępu (ACL) do pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2ee7d-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2ee7d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ee7d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee7d-108">Przykład 1. Pobieranie listy ACL dla folderu</span><span class="sxs-lookup"><span data-stu-id="2ee7d-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="2ee7d-109">To polecenie pobiera listę ACL katalogu głównego określonego konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="2ee7d-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="2ee7d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ee7d-110">PARAMETERS</span></span>

### <span data-ttu-id="2ee7d-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="2ee7d-111">-Account</span></span>
<span data-ttu-id="2ee7d-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2ee7d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2ee7d-113">-Path</span><span class="sxs-lookup"><span data-stu-id="2ee7d-113">-Path</span></span>
<span data-ttu-id="2ee7d-114">Określa ścieżkę do usługi Data Lake Store elementu, dla którego to polecenie cmdlet pobiera wpis ACE, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="2ee7d-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2ee7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee7d-115">-DefaultProfile</span></span>
<span data-ttu-id="2ee7d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee7d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee7d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee7d-117">CommonParameters</span></span>
<span data-ttu-id="2ee7d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee7d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee7d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee7d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee7d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ee7d-120">INPUTS</span></span>

## <span data-ttu-id="2ee7d-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ee7d-121">OUTPUTS</span></span>

### <span data-ttu-id="2ee7d-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="2ee7d-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="2ee7d-123">Lista wpisów list ACL dla określonego folderu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="2ee7d-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="2ee7d-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ee7d-124">NOTES</span></span>

## <span data-ttu-id="2ee7d-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ee7d-125">RELATED LINKS</span></span>

[<span data-ttu-id="2ee7d-126">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2ee7d-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="2ee7d-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2ee7d-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


