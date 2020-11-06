---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551051"
---
# <span data-ttu-id="e834a-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="e834a-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="e834a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e834a-102">SYNOPSIS</span></span>
<span data-ttu-id="e834a-103">Pobiera liczbę ósemkową do pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e834a-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e834a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e834a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e834a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e834a-105">DESCRIPTION</span></span>
<span data-ttu-id="e834a-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemPermission** Pobiera liczbę ósemkową pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e834a-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e834a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e834a-107">EXAMPLES</span></span>

### <span data-ttu-id="e834a-108">Przykład 1: Ustawianie liczby ósemkowej uprawnień dla pliku</span><span class="sxs-lookup"><span data-stu-id="e834a-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="e834a-109">To polecenie pobiera liczbę ósemkową o uprawnienia dla pliku.</span><span class="sxs-lookup"><span data-stu-id="e834a-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="e834a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e834a-110">PARAMETERS</span></span>

### <span data-ttu-id="e834a-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e834a-111">-Account</span></span>
<span data-ttu-id="e834a-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e834a-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="e834a-113">-Path</span><span class="sxs-lookup"><span data-stu-id="e834a-113">-Path</span></span>
<span data-ttu-id="e834a-114">Określa ścieżkę pliku lub folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e834a-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e834a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e834a-115">-DefaultProfile</span></span>
<span data-ttu-id="e834a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e834a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e834a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e834a-117">CommonParameters</span></span>
<span data-ttu-id="e834a-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e834a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e834a-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e834a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e834a-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e834a-120">INPUTS</span></span>

## <span data-ttu-id="e834a-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e834a-121">OUTPUTS</span></span>

### <span data-ttu-id="e834a-122">ciąg</span><span class="sxs-lookup"><span data-stu-id="e834a-122">string</span></span>
<span data-ttu-id="e834a-123">Tekst reprezentujący własność ósemkową</span><span class="sxs-lookup"><span data-stu-id="e834a-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="e834a-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e834a-124">NOTES</span></span>
* <span data-ttu-id="e834a-125">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="e834a-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="e834a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e834a-126">RELATED LINKS</span></span>

[<span data-ttu-id="e834a-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="e834a-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


