---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198130"
---
# <span data-ttu-id="4459f-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4459f-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4459f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4459f-102">SYNOPSIS</span></span>
<span data-ttu-id="4459f-103">Pobiera określonego zaufanego dostawcę tożsamości w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4459f-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="4459f-104">Jeśli nie określono żadnego dostawcy, jest to lista wszystkich dostawców dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="4459f-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="4459f-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4459f-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4459f-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="4459f-106">DESCRIPTION</span></span>
<span data-ttu-id="4459f-107">Polecenie **cmdlet Get-AzDataLakeStoreTrustedIdProvider** pobiera określonego zaufanego dostawcę tożsamości w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4459f-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="4459f-108">Jeśli nie określono żadnego dostawcy, jest to lista wszystkich dostawców dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="4459f-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="4459f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4459f-109">EXAMPLES</span></span>

### <span data-ttu-id="4459f-110">Przykład 1. Uzyskiwanie konkretnego zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="4459f-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="4459f-111">Zwraca dostawcę o nazwie "MyProvider" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="4459f-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="4459f-112">Przykład 2. Lista wszystkich dostawców na koncie</span><span class="sxs-lookup"><span data-stu-id="4459f-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="4459f-113">Lista wszystkich dostawców w obszarze konta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="4459f-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="4459f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4459f-114">PARAMETERS</span></span>

### <span data-ttu-id="4459f-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="4459f-115">-Account</span></span>
<span data-ttu-id="4459f-116">Konto usługi Data Lake Store w celu pobrania zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="4459f-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="4459f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4459f-117">-DefaultProfile</span></span>
<span data-ttu-id="4459f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4459f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4459f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4459f-119">-Name</span></span>
<span data-ttu-id="4459f-120">Nazwa zaufanego dostawcy tożsamości do pobrania</span><span class="sxs-lookup"><span data-stu-id="4459f-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4459f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4459f-121">-ResourceGroupName</span></span>
<span data-ttu-id="4459f-122">Nazwa grupy zasobów, w ramach której chcesz pobrać określonego dostawcę zaufanych tożsamości dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="4459f-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4459f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4459f-123">CommonParameters</span></span>
<span data-ttu-id="4459f-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4459f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4459f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4459f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4459f-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4459f-126">INPUTS</span></span>

### <span data-ttu-id="4459f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4459f-127">System.String</span></span>

## <span data-ttu-id="4459f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4459f-128">OUTPUTS</span></span>

### <span data-ttu-id="4459f-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4459f-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4459f-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4459f-130">NOTES</span></span>

## <span data-ttu-id="4459f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4459f-131">RELATED LINKS</span></span>
