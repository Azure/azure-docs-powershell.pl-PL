---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 886c8e7227d036e67d3e6f0d2dc04c4e9887e777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542635"
---
# <span data-ttu-id="592d8-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="592d8-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="592d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="592d8-102">SYNOPSIS</span></span>
<span data-ttu-id="592d8-103">Pobiera właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="592d8-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="592d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="592d8-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="592d8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="592d8-105">DESCRIPTION</span></span>
<span data-ttu-id="592d8-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemOwner** Pobiera właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="592d8-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="592d8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="592d8-107">EXAMPLES</span></span>

### <span data-ttu-id="592d8-108">Przykład 1. Uzyskaj właścicielowi katalogu</span><span class="sxs-lookup"><span data-stu-id="592d8-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="592d8-109">To polecenie uzyskuje właściciela dla katalogu głównego konta usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="592d8-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="592d8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="592d8-110">PARAMETERS</span></span>

### <span data-ttu-id="592d8-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="592d8-111">-Account</span></span>
<span data-ttu-id="592d8-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="592d8-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="592d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592d8-113">-DefaultProfile</span></span>
<span data-ttu-id="592d8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="592d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="592d8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="592d8-115">-Path</span></span>
<span data-ttu-id="592d8-116">Określa ścieżkę elementu Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="592d8-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592d8-117">-Type</span><span class="sxs-lookup"><span data-stu-id="592d8-117">-Type</span></span>
<span data-ttu-id="592d8-118">Określa typ właściciela do pobrania.</span><span class="sxs-lookup"><span data-stu-id="592d8-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="592d8-119">Dopuszczalne wartości tego parametru to: użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="592d8-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592d8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592d8-120">CommonParameters</span></span>
<span data-ttu-id="592d8-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592d8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592d8-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="592d8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592d8-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="592d8-123">INPUTS</span></span>

### <span data-ttu-id="592d8-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="592d8-124">None</span></span>
<span data-ttu-id="592d8-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="592d8-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="592d8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="592d8-126">OUTPUTS</span></span>

### <span data-ttu-id="592d8-127">ciąg</span><span class="sxs-lookup"><span data-stu-id="592d8-127">string</span></span>
<span data-ttu-id="592d8-128">Właściciel określonego elementu.</span><span class="sxs-lookup"><span data-stu-id="592d8-128">The owner of the specified item.</span></span>

## <span data-ttu-id="592d8-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="592d8-129">NOTES</span></span>

## <span data-ttu-id="592d8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="592d8-130">RELATED LINKS</span></span>

[<span data-ttu-id="592d8-131">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="592d8-131">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


