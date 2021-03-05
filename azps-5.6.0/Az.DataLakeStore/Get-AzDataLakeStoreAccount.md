---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 845fbb645ca9ba3495aa0dcf2b56cdbd793630e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963098"
---
# <span data-ttu-id="6a821-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6a821-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="6a821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a821-102">SYNOPSIS</span></span>
<span data-ttu-id="6a821-103">Pobiera szczegółowe informacje o koncie w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a821-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6a821-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a821-104">SYNTAX</span></span>

### <span data-ttu-id="6a821-105">GetAllInSubscription (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6a821-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a821-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a821-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a821-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="6a821-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a821-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a821-108">DESCRIPTION</span></span>
<span data-ttu-id="6a821-109">Polecenie **cmdlet Get-AzDataLakeStoreAccount** pobiera szczegóły dotyczące konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a821-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6a821-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a821-110">EXAMPLES</span></span>

### <span data-ttu-id="6a821-111">Przykład 1. Uzyskiwanie konta w sklepie Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6a821-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="6a821-112">To polecenie pobiera konto o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6a821-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="6a821-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a821-113">PARAMETERS</span></span>

### <span data-ttu-id="6a821-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a821-114">-DefaultProfile</span></span>
<span data-ttu-id="6a821-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6a821-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a821-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6a821-116">-Name</span></span>
<span data-ttu-id="6a821-117">Określa nazwę konta do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="6a821-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="6a821-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a821-118">-ResourceGroupName</span></span>
<span data-ttu-id="6a821-119">Określa nazwę grupy zasobów, która zawiera konto Data Lake Store do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="6a821-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="6a821-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a821-120">CommonParameters</span></span>
<span data-ttu-id="6a821-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a821-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a821-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a821-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a821-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a821-123">INPUTS</span></span>

### <span data-ttu-id="6a821-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6a821-124">System.String</span></span>

## <span data-ttu-id="6a821-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a821-125">OUTPUTS</span></span>

### <span data-ttu-id="6a821-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6a821-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="6a821-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a821-127">NOTES</span></span>

## <span data-ttu-id="6a821-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a821-128">RELATED LINKS</span></span>

[<span data-ttu-id="6a821-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6a821-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6a821-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6a821-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6a821-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6a821-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6a821-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6a821-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


