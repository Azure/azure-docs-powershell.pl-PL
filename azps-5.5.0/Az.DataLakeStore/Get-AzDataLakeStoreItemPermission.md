---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177091"
---
# <span data-ttu-id="0f176-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0f176-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="0f176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f176-102">SYNOPSIS</span></span>
<span data-ttu-id="0f176-103">Pobiera ósemkową ósemkową nazwę pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f176-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0f176-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f176-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f176-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f176-105">DESCRIPTION</span></span>
<span data-ttu-id="0f176-106">Polecenie **cmdlet Get-AzDataLakeStoreItemPermission** pobiera ósemkową ósemkę uprawnień do pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f176-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0f176-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f176-107">EXAMPLES</span></span>

### <span data-ttu-id="0f176-108">Przykład 1. Ustawianie ósemkowej uprawnień dla pliku</span><span class="sxs-lookup"><span data-stu-id="0f176-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="0f176-109">To polecenie pobiera ósemkową ósemkową uprawnienie do pliku.</span><span class="sxs-lookup"><span data-stu-id="0f176-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="0f176-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f176-110">PARAMETERS</span></span>

### <span data-ttu-id="0f176-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="0f176-111">-Account</span></span>
<span data-ttu-id="0f176-112">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f176-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="0f176-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f176-113">-DefaultProfile</span></span>
<span data-ttu-id="0f176-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f176-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f176-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="0f176-115">-Path</span></span>
<span data-ttu-id="0f176-116">Określa ścieżkę pliku lub folderu do magazynu Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="0f176-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0f176-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f176-117">CommonParameters</span></span>
<span data-ttu-id="0f176-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f176-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f176-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f176-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f176-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f176-120">INPUTS</span></span>

### <span data-ttu-id="0f176-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0f176-121">System.String</span></span>

### <span data-ttu-id="0f176-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0f176-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="0f176-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f176-123">OUTPUTS</span></span>

### <span data-ttu-id="0f176-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0f176-124">System.String</span></span>

## <span data-ttu-id="0f176-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f176-125">NOTES</span></span>
* <span data-ttu-id="0f176-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0f176-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="0f176-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f176-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f176-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0f176-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


