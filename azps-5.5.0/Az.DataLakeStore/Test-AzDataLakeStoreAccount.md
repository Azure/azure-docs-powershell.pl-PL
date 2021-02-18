---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180891"
---
# <span data-ttu-id="e622a-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e622a-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e622a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e622a-102">SYNOPSIS</span></span>
<span data-ttu-id="e622a-103">Sprawdza istnienie konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e622a-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e622a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e622a-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e622a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e622a-105">DESCRIPTION</span></span>
<span data-ttu-id="e622a-106">Polecenie **cmdlet Test-AzDataLakeStoreAccount** sprawdza istnienie konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e622a-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e622a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e622a-107">EXAMPLES</span></span>

### <span data-ttu-id="e622a-108">Przykład 1. Testowanie konta</span><span class="sxs-lookup"><span data-stu-id="e622a-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e622a-109">To polecenie sprawdza, czy istnieje konto o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="e622a-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="e622a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e622a-110">PARAMETERS</span></span>

### <span data-ttu-id="e622a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e622a-111">-DefaultProfile</span></span>
<span data-ttu-id="e622a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e622a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e622a-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e622a-113">-Name</span></span>
<span data-ttu-id="e622a-114">Określa nazwę konta data lake store do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="e622a-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e622a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e622a-115">-ResourceGroupName</span></span>
<span data-ttu-id="e622a-116">Określa nazwę grupy zasobów zawierającej konto do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="e622a-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="e622a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e622a-117">CommonParameters</span></span>
<span data-ttu-id="e622a-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e622a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e622a-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e622a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e622a-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e622a-120">INPUTS</span></span>

### <span data-ttu-id="e622a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e622a-121">System.String</span></span>

## <span data-ttu-id="e622a-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e622a-122">OUTPUTS</span></span>

### <span data-ttu-id="e622a-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e622a-123">System.Boolean</span></span>

## <span data-ttu-id="e622a-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e622a-124">NOTES</span></span>

## <span data-ttu-id="e622a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e622a-125">RELATED LINKS</span></span>

[<span data-ttu-id="e622a-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e622a-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e622a-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e622a-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e622a-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e622a-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e622a-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e622a-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


