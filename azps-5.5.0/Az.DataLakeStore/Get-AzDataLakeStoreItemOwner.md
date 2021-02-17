---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177090"
---
# <span data-ttu-id="8f4cb-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="8f4cb-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="8f4cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4cb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4cb-103">Pobiera właściciela pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8f4cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f4cb-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f4cb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f4cb-105">DESCRIPTION</span></span>
<span data-ttu-id="8f4cb-106">Polecenie **cmdlet Get-AzDataLakeStoreItemOwner** pobiera właściciela pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8f4cb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f4cb-107">EXAMPLES</span></span>

### <span data-ttu-id="8f4cb-108">Przykład 1. Uzyskiwanie właściciela katalogu</span><span class="sxs-lookup"><span data-stu-id="8f4cb-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="8f4cb-109">To polecenie pobiera właściciela katalogu głównego konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="8f4cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f4cb-110">PARAMETERS</span></span>

### <span data-ttu-id="8f4cb-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="8f4cb-111">-Account</span></span>
<span data-ttu-id="8f4cb-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8f4cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4cb-113">-DefaultProfile</span></span>
<span data-ttu-id="8f4cb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f4cb-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="8f4cb-115">-Path</span></span>
<span data-ttu-id="8f4cb-116">Określa ścieżkę elementu do magazynu Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="8f4cb-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8f4cb-117">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="8f4cb-117">-Type</span></span>
<span data-ttu-id="8f4cb-118">Określa typ właściciela do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="8f4cb-119">Dopuszczalne wartości dla tego parametru to: Użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4cb-120">CommonParameters</span></span>
<span data-ttu-id="8f4cb-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4cb-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4cb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4cb-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f4cb-123">INPUTS</span></span>

### <span data-ttu-id="8f4cb-124">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4cb-124">System.String</span></span>

### <span data-ttu-id="8f4cb-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8f4cb-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8f4cb-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Właściciel</span><span class="sxs-lookup"><span data-stu-id="8f4cb-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="8f4cb-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f4cb-127">OUTPUTS</span></span>

### <span data-ttu-id="8f4cb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4cb-128">System.String</span></span>

## <span data-ttu-id="8f4cb-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f4cb-129">NOTES</span></span>

## <span data-ttu-id="8f4cb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f4cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="8f4cb-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="8f4cb-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


