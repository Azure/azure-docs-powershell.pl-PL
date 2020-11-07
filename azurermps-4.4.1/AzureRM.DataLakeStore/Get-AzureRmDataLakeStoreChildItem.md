---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 51b27c5dcffc36e45946d9fd2b0c842cfe17cdaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718227"
---
# <span data-ttu-id="75e3c-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="75e3c-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="75e3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="75e3c-103">Pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="75e3c-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75e3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75e3c-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75e3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75e3c-105">DESCRIPTION</span></span>
<span data-ttu-id="75e3c-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreChildItem** pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="75e3c-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="75e3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75e3c-107">EXAMPLES</span></span>

### <span data-ttu-id="75e3c-108">Przykład 1. Pobieranie elementów podrzędnych folderu</span><span class="sxs-lookup"><span data-stu-id="75e3c-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="75e3c-109">To polecenie pobiera elementy podrzędne folderu Moje pliki.</span><span class="sxs-lookup"><span data-stu-id="75e3c-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="75e3c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75e3c-110">PARAMETERS</span></span>

### <span data-ttu-id="75e3c-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="75e3c-111">-Account</span></span>
<span data-ttu-id="75e3c-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="75e3c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="75e3c-113">-Path</span><span class="sxs-lookup"><span data-stu-id="75e3c-113">-Path</span></span>
<span data-ttu-id="75e3c-114">Określa ścieżkę folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="75e3c-114">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e3c-115">-DefaultProfile</span></span>
<span data-ttu-id="75e3c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75e3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75e3c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e3c-117">CommonParameters</span></span>
<span data-ttu-id="75e3c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e3c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e3c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e3c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e3c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75e3c-120">INPUTS</span></span>

## <span data-ttu-id="75e3c-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75e3c-121">OUTPUTS</span></span>

### <span data-ttu-id="75e3c-122">IEnumerable<DataLakeStoreItem></span><span class="sxs-lookup"><span data-stu-id="75e3c-122">IEnumerable<DataLakeStoreItem></span></span>
<span data-ttu-id="75e3c-123">Lista plików i folderów usługi Data Lake Store pod określoną ścieżką.</span><span class="sxs-lookup"><span data-stu-id="75e3c-123">The list of Data Lake Store files and folders under the specified path.</span></span>

## <span data-ttu-id="75e3c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75e3c-124">NOTES</span></span>

## <span data-ttu-id="75e3c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75e3c-125">RELATED LINKS</span></span>

