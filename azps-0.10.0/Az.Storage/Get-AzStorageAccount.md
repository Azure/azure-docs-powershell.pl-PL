---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: be32e761fc854c6ad4a270f36e4c9b6328e00ba1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892281"
---
# <span data-ttu-id="37a12-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a12-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="37a12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37a12-102">SYNOPSIS</span></span>
<span data-ttu-id="37a12-103">Pobiera konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="37a12-103">Gets a Storage account.</span></span>

## <span data-ttu-id="37a12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37a12-104">SYNTAX</span></span>

### <span data-ttu-id="37a12-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="37a12-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37a12-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37a12-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a12-107">Opis</span><span class="sxs-lookup"><span data-stu-id="37a12-107">DESCRIPTION</span></span>
<span data-ttu-id="37a12-108">Polecenie cmdlet **Get-AzStorageAccount** pobiera określone konto magazynu lub wszystkie konta magazynu w grupie zasobów lub abonament.</span><span class="sxs-lookup"><span data-stu-id="37a12-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="37a12-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37a12-109">EXAMPLES</span></span>

### <span data-ttu-id="37a12-110">Przykład 1: uzyskiwanie określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="37a12-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="37a12-111">To polecenie pobiera określone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="37a12-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="37a12-112">Przykład 2: pobieranie wszystkich kont magazynu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="37a12-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="37a12-113">To polecenie umożliwia pobieranie wszystkich kont magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="37a12-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="37a12-114">Przykład 3: uzyskiwanie wszystkich kont magazynu w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="37a12-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="37a12-115">To polecenie umożliwia pobieranie wszystkich kont magazynu w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="37a12-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="37a12-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37a12-116">PARAMETERS</span></span>

### <span data-ttu-id="37a12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a12-117">-DefaultProfile</span></span>
<span data-ttu-id="37a12-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37a12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37a12-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37a12-119">-Name</span></span>
<span data-ttu-id="37a12-120">Określa nazwę konta magazynu, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="37a12-120">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a12-121">-ResourceGroupName</span></span>
<span data-ttu-id="37a12-122">Określa nazwę grupy zasobów zawierającej konto magazynu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="37a12-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a12-123">CommonParameters</span></span>
<span data-ttu-id="37a12-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a12-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a12-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a12-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37a12-126">INPUTS</span></span>

### <span data-ttu-id="37a12-127">System. String</span><span class="sxs-lookup"><span data-stu-id="37a12-127">System.String</span></span>

## <span data-ttu-id="37a12-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37a12-128">OUTPUTS</span></span>

### <span data-ttu-id="37a12-129">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a12-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="37a12-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37a12-130">NOTES</span></span>

## <span data-ttu-id="37a12-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37a12-131">RELATED LINKS</span></span>

[<span data-ttu-id="37a12-132">Nowe — AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a12-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="37a12-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a12-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="37a12-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37a12-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


