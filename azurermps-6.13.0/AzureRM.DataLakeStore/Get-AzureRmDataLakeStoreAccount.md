---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524473"
---
# <span data-ttu-id="9f5f7-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f5f7-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="9f5f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5f7-103">Pobiera szczegóły konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f5f7-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f5f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f5f7-104">SYNTAX</span></span>

### <span data-ttu-id="9f5f7-105">GetAllInSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9f5f7-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f5f7-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f5f7-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f5f7-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="9f5f7-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f5f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9f5f7-108">DESCRIPTION</span></span>
<span data-ttu-id="9f5f7-109">Polecenie cmdlet **Get-AzureRmDataLakeStoreAccount** pobiera szczegóły konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f5f7-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="9f5f7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f5f7-110">EXAMPLES</span></span>

### <span data-ttu-id="9f5f7-111">Przykład 1: Uzyskiwanie konta w usłudze Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9f5f7-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="9f5f7-112">To polecenie uzyskuje konto o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="9f5f7-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="9f5f7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f5f7-113">PARAMETERS</span></span>

### <span data-ttu-id="9f5f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5f7-114">-DefaultProfile</span></span>
<span data-ttu-id="9f5f7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9f5f7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f5f7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9f5f7-116">-Name</span></span>
<span data-ttu-id="9f5f7-117">Określa nazwę konta, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="9f5f7-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5f7-118">-ResourceGroupName</span></span>
<span data-ttu-id="9f5f7-119">Określa nazwę grupy zasobów zawierającej konto usługi Data Lake Store, które ma zostać nadane.</span><span class="sxs-lookup"><span data-stu-id="9f5f7-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5f7-120">CommonParameters</span></span>
<span data-ttu-id="9f5f7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5f7-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5f7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5f7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f5f7-123">INPUTS</span></span>

### <span data-ttu-id="9f5f7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9f5f7-124">System.String</span></span>

## <span data-ttu-id="9f5f7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f5f7-125">OUTPUTS</span></span>

### <span data-ttu-id="9f5f7-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f5f7-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="9f5f7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f5f7-127">NOTES</span></span>

## <span data-ttu-id="9f5f7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f5f7-128">RELATED LINKS</span></span>

[<span data-ttu-id="9f5f7-129">Nowe — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f5f7-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9f5f7-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f5f7-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9f5f7-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f5f7-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9f5f7-132">Test — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f5f7-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


