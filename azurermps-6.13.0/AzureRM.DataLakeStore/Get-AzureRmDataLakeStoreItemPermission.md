---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 6aeae8333cc8aa5a394abfaba68dcc0d7fb732f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541727"
---
# <span data-ttu-id="ac30d-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="ac30d-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="ac30d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac30d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac30d-103">Pobiera liczbę ósemkową do pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ac30d-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac30d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac30d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac30d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac30d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac30d-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemPermission** Pobiera liczbę ósemkową pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ac30d-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ac30d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac30d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac30d-108">Przykład 1: Ustawianie liczby ósemkowej uprawnień dla pliku</span><span class="sxs-lookup"><span data-stu-id="ac30d-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="ac30d-109">To polecenie pobiera liczbę ósemkową o uprawnienia dla pliku.</span><span class="sxs-lookup"><span data-stu-id="ac30d-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="ac30d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac30d-110">PARAMETERS</span></span>

### <span data-ttu-id="ac30d-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ac30d-111">-Account</span></span>
<span data-ttu-id="ac30d-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ac30d-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="ac30d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac30d-113">-DefaultProfile</span></span>
<span data-ttu-id="ac30d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac30d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac30d-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ac30d-115">-Path</span></span>
<span data-ttu-id="ac30d-116">Określa ścieżkę pliku lub folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="ac30d-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ac30d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac30d-117">CommonParameters</span></span>
<span data-ttu-id="ac30d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac30d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac30d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac30d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac30d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac30d-120">INPUTS</span></span>

### <span data-ttu-id="ac30d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ac30d-121">System.String</span></span>

### <span data-ttu-id="ac30d-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ac30d-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="ac30d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac30d-123">OUTPUTS</span></span>

### <span data-ttu-id="ac30d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ac30d-124">System.String</span></span>
<span data-ttu-id="ac30d-125">Tekst reprezentujący własność ósemkową</span><span class="sxs-lookup"><span data-stu-id="ac30d-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="ac30d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac30d-126">NOTES</span></span>
* <span data-ttu-id="ac30d-127">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="ac30d-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="ac30d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac30d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ac30d-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="ac30d-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


