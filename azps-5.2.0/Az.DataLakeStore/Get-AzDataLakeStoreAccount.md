---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371394"
---
# <span data-ttu-id="9e044-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9e044-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="9e044-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e044-102">SYNOPSIS</span></span>
<span data-ttu-id="9e044-103">Pobiera szczegóły konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e044-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="9e044-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e044-104">SYNTAX</span></span>

### <span data-ttu-id="9e044-105">GetAllInSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e044-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e044-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e044-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e044-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="9e044-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e044-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9e044-108">DESCRIPTION</span></span>
<span data-ttu-id="9e044-109">Polecenie cmdlet **Get-AzDataLakeStoreAccount** pobiera szczegóły konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e044-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="9e044-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e044-110">EXAMPLES</span></span>

### <span data-ttu-id="9e044-111">Przykład 1: Uzyskiwanie konta w usłudze Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9e044-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="9e044-112">To polecenie uzyskuje konto o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="9e044-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="9e044-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e044-113">PARAMETERS</span></span>

### <span data-ttu-id="9e044-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e044-114">-DefaultProfile</span></span>
<span data-ttu-id="9e044-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e044-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e044-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e044-116">-Name</span></span>
<span data-ttu-id="9e044-117">Określa nazwę konta, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="9e044-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="9e044-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e044-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e044-119">Określa nazwę grupy zasobów zawierającej konto usługi Data Lake Store, które ma zostać nadane.</span><span class="sxs-lookup"><span data-stu-id="9e044-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="9e044-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e044-120">CommonParameters</span></span>
<span data-ttu-id="9e044-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e044-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e044-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e044-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e044-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e044-123">INPUTS</span></span>

### <span data-ttu-id="9e044-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9e044-124">System.String</span></span>

## <span data-ttu-id="9e044-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e044-125">OUTPUTS</span></span>

### <span data-ttu-id="9e044-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9e044-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="9e044-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e044-127">NOTES</span></span>

## <span data-ttu-id="9e044-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e044-128">RELATED LINKS</span></span>

[<span data-ttu-id="9e044-129">Nowe — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9e044-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9e044-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9e044-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9e044-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9e044-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9e044-132">Test — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9e044-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


