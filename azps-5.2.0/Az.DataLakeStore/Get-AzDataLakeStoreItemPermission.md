---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343858"
---
# <span data-ttu-id="808bf-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="808bf-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="808bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="808bf-102">SYNOPSIS</span></span>
<span data-ttu-id="808bf-103">Pobiera liczbę ósemkową do pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="808bf-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="808bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="808bf-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="808bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="808bf-105">DESCRIPTION</span></span>
<span data-ttu-id="808bf-106">Polecenie cmdlet **Get-AzDataLakeStoreItemPermission** Pobiera liczbę ósemkową pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="808bf-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="808bf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="808bf-107">EXAMPLES</span></span>

### <span data-ttu-id="808bf-108">Przykład 1: Ustawianie liczby ósemkowej uprawnień dla pliku</span><span class="sxs-lookup"><span data-stu-id="808bf-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="808bf-109">To polecenie pobiera liczbę ósemkową o uprawnienia dla pliku.</span><span class="sxs-lookup"><span data-stu-id="808bf-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="808bf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="808bf-110">PARAMETERS</span></span>

### <span data-ttu-id="808bf-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="808bf-111">-Account</span></span>
<span data-ttu-id="808bf-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="808bf-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="808bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808bf-113">-DefaultProfile</span></span>
<span data-ttu-id="808bf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="808bf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="808bf-115">-Path</span><span class="sxs-lookup"><span data-stu-id="808bf-115">-Path</span></span>
<span data-ttu-id="808bf-116">Określa ścieżkę pliku lub folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="808bf-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="808bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808bf-117">CommonParameters</span></span>
<span data-ttu-id="808bf-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808bf-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808bf-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808bf-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="808bf-120">INPUTS</span></span>

### <span data-ttu-id="808bf-121">System. String</span><span class="sxs-lookup"><span data-stu-id="808bf-121">System.String</span></span>

### <span data-ttu-id="808bf-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="808bf-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="808bf-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="808bf-123">OUTPUTS</span></span>

### <span data-ttu-id="808bf-124">System. String</span><span class="sxs-lookup"><span data-stu-id="808bf-124">System.String</span></span>

## <span data-ttu-id="808bf-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="808bf-125">NOTES</span></span>
* <span data-ttu-id="808bf-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="808bf-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="808bf-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="808bf-127">RELATED LINKS</span></span>

[<span data-ttu-id="808bf-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="808bf-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


