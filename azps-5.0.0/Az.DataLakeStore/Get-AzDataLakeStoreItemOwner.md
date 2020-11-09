---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305604"
---
# <span data-ttu-id="6e5f0-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6e5f0-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="6e5f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5f0-103">Pobiera właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6e5f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e5f0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e5f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e5f0-105">DESCRIPTION</span></span>
<span data-ttu-id="6e5f0-106">Polecenie cmdlet **Get-AzDataLakeStoreItemOwner** Pobiera właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6e5f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e5f0-107">EXAMPLES</span></span>

### <span data-ttu-id="6e5f0-108">Przykład 1. Uzyskaj właścicielowi katalogu</span><span class="sxs-lookup"><span data-stu-id="6e5f0-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="6e5f0-109">To polecenie uzyskuje właściciela dla katalogu głównego konta usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="6e5f0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e5f0-110">PARAMETERS</span></span>

### <span data-ttu-id="6e5f0-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="6e5f0-111">-Account</span></span>
<span data-ttu-id="6e5f0-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6e5f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5f0-113">-DefaultProfile</span></span>
<span data-ttu-id="6e5f0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e5f0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="6e5f0-115">-Path</span></span>
<span data-ttu-id="6e5f0-116">Określa ścieżkę elementu Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="6e5f0-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6e5f0-117">-Type</span><span class="sxs-lookup"><span data-stu-id="6e5f0-117">-Type</span></span>
<span data-ttu-id="6e5f0-118">Określa typ właściciela do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="6e5f0-119">Dopuszczalne wartości tego parametru to: użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="6e5f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5f0-120">CommonParameters</span></span>
<span data-ttu-id="6e5f0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e5f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5f0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e5f0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5f0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e5f0-123">INPUTS</span></span>

### <span data-ttu-id="6e5f0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6e5f0-124">System.String</span></span>

### <span data-ttu-id="6e5f0-125">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6e5f0-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6e5f0-126">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="6e5f0-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="6e5f0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e5f0-127">OUTPUTS</span></span>

### <span data-ttu-id="6e5f0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6e5f0-128">System.String</span></span>

## <span data-ttu-id="6e5f0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e5f0-129">NOTES</span></span>

## <span data-ttu-id="6e5f0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e5f0-130">RELATED LINKS</span></span>

[<span data-ttu-id="6e5f0-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6e5f0-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


