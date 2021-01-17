---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372813"
---
# <span data-ttu-id="6e745-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6e745-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="6e745-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e745-102">SYNOPSIS</span></span>
<span data-ttu-id="6e745-103">Testowanie istnienia konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e745-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="6e745-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e745-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e745-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e745-105">DESCRIPTION</span></span>
<span data-ttu-id="6e745-106">Polecenie cmdlet **test-AzDataLakeStoreAccount** sprawdza istnienie konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e745-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="6e745-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e745-107">EXAMPLES</span></span>

### <span data-ttu-id="6e745-108">Przykład 1: testowanie konta</span><span class="sxs-lookup"><span data-stu-id="6e745-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="6e745-109">To polecenie sprawdza, czy konto o nazwie ContosoADL istnieje.</span><span class="sxs-lookup"><span data-stu-id="6e745-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="6e745-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e745-110">PARAMETERS</span></span>

### <span data-ttu-id="6e745-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e745-111">-DefaultProfile</span></span>
<span data-ttu-id="6e745-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6e745-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e745-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e745-113">-Name</span></span>
<span data-ttu-id="6e745-114">Określa nazwę konta usługi Data Lake Store do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="6e745-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="6e745-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e745-115">-ResourceGroupName</span></span>
<span data-ttu-id="6e745-116">Określa nazwę grupy zasobów zawierającej konto do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="6e745-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="6e745-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e745-117">CommonParameters</span></span>
<span data-ttu-id="6e745-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e745-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e745-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e745-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e745-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e745-120">INPUTS</span></span>

### <span data-ttu-id="6e745-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6e745-121">System.String</span></span>

## <span data-ttu-id="6e745-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e745-122">OUTPUTS</span></span>

### <span data-ttu-id="6e745-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e745-123">System.Boolean</span></span>

## <span data-ttu-id="6e745-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e745-124">NOTES</span></span>

## <span data-ttu-id="6e745-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e745-125">RELATED LINKS</span></span>

[<span data-ttu-id="6e745-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6e745-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6e745-127">Nowe — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6e745-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6e745-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6e745-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6e745-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6e745-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


