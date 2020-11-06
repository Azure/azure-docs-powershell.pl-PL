---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 6477a9f8c3830fa8ca8a74780db560455eb61dfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548131"
---
# <span data-ttu-id="141a1-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="141a1-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="141a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="141a1-102">SYNOPSIS</span></span>
<span data-ttu-id="141a1-103">Pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="141a1-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="141a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="141a1-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="141a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="141a1-105">DESCRIPTION</span></span>
<span data-ttu-id="141a1-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreChildItem** pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="141a1-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="141a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="141a1-107">EXAMPLES</span></span>

### <span data-ttu-id="141a1-108">Przykład 1. Pobieranie elementów podrzędnych folderu</span><span class="sxs-lookup"><span data-stu-id="141a1-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="141a1-109">To polecenie pobiera elementy podrzędne folderu Moje pliki.</span><span class="sxs-lookup"><span data-stu-id="141a1-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="141a1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="141a1-110">PARAMETERS</span></span>

### <span data-ttu-id="141a1-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="141a1-111">-Account</span></span>
<span data-ttu-id="141a1-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="141a1-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141a1-113">-DefaultProfile</span></span>
<span data-ttu-id="141a1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="141a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141a1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="141a1-115">-Path</span></span>
<span data-ttu-id="141a1-116">Określa ścieżkę folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="141a1-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141a1-117">CommonParameters</span></span>
<span data-ttu-id="141a1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141a1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="141a1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141a1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="141a1-120">INPUTS</span></span>

### <span data-ttu-id="141a1-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="141a1-121">None</span></span>
<span data-ttu-id="141a1-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="141a1-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="141a1-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="141a1-123">OUTPUTS</span></span>

### <span data-ttu-id="141a1-124">IEnumerable<DataLakeStoreItem></span><span class="sxs-lookup"><span data-stu-id="141a1-124">IEnumerable<DataLakeStoreItem></span></span>
<span data-ttu-id="141a1-125">Lista plików i folderów usługi Data Lake Store pod określoną ścieżką.</span><span class="sxs-lookup"><span data-stu-id="141a1-125">The list of Data Lake Store files and folders under the specified path.</span></span>

## <span data-ttu-id="141a1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="141a1-126">NOTES</span></span>

## <span data-ttu-id="141a1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="141a1-127">RELATED LINKS</span></span>

