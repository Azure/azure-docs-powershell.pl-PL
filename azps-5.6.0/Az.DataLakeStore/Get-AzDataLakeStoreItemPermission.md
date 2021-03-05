---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 0754160aa375ba84ac469771a97f792c36b51ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985195"
---
# <span data-ttu-id="39d9e-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="39d9e-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="39d9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="39d9e-103">Pobiera ósemkową ósemkową nazwę pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39d9e-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="39d9e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39d9e-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39d9e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="39d9e-106">Polecenie **cmdlet Get-AzDataLakeStoreItemPermission** pobiera ósemkową ósemkę uprawnień pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39d9e-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="39d9e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="39d9e-108">Przykład 1. Ustawianie ósemkowej uprawnień dla pliku</span><span class="sxs-lookup"><span data-stu-id="39d9e-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="39d9e-109">To polecenie pobiera ósemkową ósemkową uprawnienie do pliku.</span><span class="sxs-lookup"><span data-stu-id="39d9e-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="39d9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="39d9e-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="39d9e-111">-Account</span></span>
<span data-ttu-id="39d9e-112">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39d9e-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="39d9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d9e-113">-DefaultProfile</span></span>
<span data-ttu-id="39d9e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39d9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39d9e-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="39d9e-115">-Path</span></span>
<span data-ttu-id="39d9e-116">Określa ścieżkę pliku lub folderu do magazynu Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="39d9e-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="39d9e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d9e-117">CommonParameters</span></span>
<span data-ttu-id="39d9e-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d9e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d9e-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d9e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d9e-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39d9e-120">INPUTS</span></span>

### <span data-ttu-id="39d9e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="39d9e-121">System.String</span></span>

### <span data-ttu-id="39d9e-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="39d9e-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="39d9e-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39d9e-123">OUTPUTS</span></span>

### <span data-ttu-id="39d9e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="39d9e-124">System.String</span></span>

## <span data-ttu-id="39d9e-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39d9e-125">NOTES</span></span>
* <span data-ttu-id="39d9e-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="39d9e-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="39d9e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39d9e-127">RELATED LINKS</span></span>

[<span data-ttu-id="39d9e-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="39d9e-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


