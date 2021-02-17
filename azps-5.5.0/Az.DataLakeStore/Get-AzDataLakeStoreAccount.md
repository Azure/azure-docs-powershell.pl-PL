---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188595"
---
# <span data-ttu-id="6cb53-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6cb53-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="6cb53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb53-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb53-103">Pobiera szczegółowe informacje o koncie w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6cb53-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6cb53-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6cb53-104">SYNTAX</span></span>

### <span data-ttu-id="6cb53-105">GetAllInSubscription (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6cb53-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cb53-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cb53-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cb53-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="6cb53-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb53-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6cb53-108">DESCRIPTION</span></span>
<span data-ttu-id="6cb53-109">Polecenie **cmdlet Get-AzDataLakeStoreAccount** pobiera szczegółowe informacje o koncie w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6cb53-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6cb53-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6cb53-110">EXAMPLES</span></span>

### <span data-ttu-id="6cb53-111">Przykład 1. Uzyskiwanie konta w sklepie Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6cb53-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="6cb53-112">To polecenie pobiera konto o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6cb53-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="6cb53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cb53-113">PARAMETERS</span></span>

### <span data-ttu-id="6cb53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb53-114">-DefaultProfile</span></span>
<span data-ttu-id="6cb53-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6cb53-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb53-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6cb53-116">-Name</span></span>
<span data-ttu-id="6cb53-117">Określa nazwę konta do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="6cb53-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="6cb53-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb53-118">-ResourceGroupName</span></span>
<span data-ttu-id="6cb53-119">Określa nazwę grupy zasobów, która zawiera konto Data Lake Store do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="6cb53-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="6cb53-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb53-120">CommonParameters</span></span>
<span data-ttu-id="6cb53-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb53-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb53-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb53-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb53-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cb53-123">INPUTS</span></span>

### <span data-ttu-id="6cb53-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6cb53-124">System.String</span></span>

## <span data-ttu-id="6cb53-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cb53-125">OUTPUTS</span></span>

### <span data-ttu-id="6cb53-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6cb53-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="6cb53-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6cb53-127">NOTES</span></span>

## <span data-ttu-id="6cb53-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cb53-128">RELATED LINKS</span></span>

[<span data-ttu-id="6cb53-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6cb53-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6cb53-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6cb53-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6cb53-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6cb53-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6cb53-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6cb53-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


