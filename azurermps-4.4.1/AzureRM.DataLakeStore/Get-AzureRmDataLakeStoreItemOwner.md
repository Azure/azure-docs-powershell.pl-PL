---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 5c36257050cccf217234a3b1ef6b89120e36b3c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718222"
---
# <span data-ttu-id="be552-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="be552-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="be552-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be552-102">SYNOPSIS</span></span>
<span data-ttu-id="be552-103">Pobiera właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="be552-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be552-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be552-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be552-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be552-105">DESCRIPTION</span></span>
<span data-ttu-id="be552-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemOwner** Pobiera właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="be552-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="be552-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be552-107">EXAMPLES</span></span>

### <span data-ttu-id="be552-108">Przykład 1. Uzyskaj właścicielowi katalogu</span><span class="sxs-lookup"><span data-stu-id="be552-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="be552-109">To polecenie uzyskuje właściciela dla katalogu głównego konta usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="be552-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="be552-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be552-110">PARAMETERS</span></span>

### <span data-ttu-id="be552-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="be552-111">-Account</span></span>
<span data-ttu-id="be552-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="be552-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="be552-113">-Path</span><span class="sxs-lookup"><span data-stu-id="be552-113">-Path</span></span>
<span data-ttu-id="be552-114">Określa ścieżkę elementu Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="be552-114">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="be552-115">-Type</span><span class="sxs-lookup"><span data-stu-id="be552-115">-Type</span></span>
<span data-ttu-id="be552-116">Określa typ właściciela do pobrania.</span><span class="sxs-lookup"><span data-stu-id="be552-116">Specifies the type of owner to get.</span></span>
<span data-ttu-id="be552-117">Dopuszczalne wartości tego parametru to: użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="be552-117">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="be552-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be552-118">-DefaultProfile</span></span>
<span data-ttu-id="be552-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be552-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be552-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be552-120">CommonParameters</span></span>
<span data-ttu-id="be552-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be552-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be552-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be552-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be552-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be552-123">INPUTS</span></span>

## <span data-ttu-id="be552-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be552-124">OUTPUTS</span></span>

### <span data-ttu-id="be552-125">ciąg</span><span class="sxs-lookup"><span data-stu-id="be552-125">string</span></span>
<span data-ttu-id="be552-126">Właściciel określonego elementu.</span><span class="sxs-lookup"><span data-stu-id="be552-126">The owner of the specified item.</span></span>

## <span data-ttu-id="be552-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be552-127">NOTES</span></span>

## <span data-ttu-id="be552-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be552-128">RELATED LINKS</span></span>

[<span data-ttu-id="be552-129">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="be552-129">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


