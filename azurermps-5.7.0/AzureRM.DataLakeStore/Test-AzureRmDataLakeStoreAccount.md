---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 15c0614094ed28a9888e2e39a6cfb81547fbb6e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551771"
---
# <span data-ttu-id="93f84-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="93f84-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="93f84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93f84-102">SYNOPSIS</span></span>
<span data-ttu-id="93f84-103">Testowanie istnienia konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93f84-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93f84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93f84-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93f84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="93f84-105">DESCRIPTION</span></span>
<span data-ttu-id="93f84-106">Polecenie cmdlet **test-AzureRmDataLakeStoreAccount** sprawdza istnienie konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93f84-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="93f84-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93f84-107">EXAMPLES</span></span>

### <span data-ttu-id="93f84-108">Przykład 1: testowanie konta</span><span class="sxs-lookup"><span data-stu-id="93f84-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="93f84-109">To polecenie sprawdza, czy konto o nazwie ContosoADL istnieje.</span><span class="sxs-lookup"><span data-stu-id="93f84-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="93f84-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93f84-110">PARAMETERS</span></span>

### <span data-ttu-id="93f84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f84-111">-DefaultProfile</span></span>
<span data-ttu-id="93f84-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="93f84-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93f84-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93f84-113">-Name</span></span>
<span data-ttu-id="93f84-114">Określa nazwę konta usługi Data Lake Store do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="93f84-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93f84-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f84-115">-ResourceGroupName</span></span>
<span data-ttu-id="93f84-116">Określa nazwę grupy zasobów zawierającej konto do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="93f84-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93f84-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f84-117">CommonParameters</span></span>
<span data-ttu-id="93f84-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f84-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f84-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f84-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f84-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93f84-120">INPUTS</span></span>

### <span data-ttu-id="93f84-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="93f84-121">None</span></span>
<span data-ttu-id="93f84-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="93f84-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93f84-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93f84-123">OUTPUTS</span></span>

### <span data-ttu-id="93f84-124">logiczną</span><span class="sxs-lookup"><span data-stu-id="93f84-124">bool</span></span>
<span data-ttu-id="93f84-125">Prawda lub FAŁSZ wskazujący istnienie określonego konta.</span><span class="sxs-lookup"><span data-stu-id="93f84-125">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="93f84-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93f84-126">NOTES</span></span>

## <span data-ttu-id="93f84-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93f84-127">RELATED LINKS</span></span>

[<span data-ttu-id="93f84-128">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="93f84-128">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="93f84-129">Nowe — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="93f84-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="93f84-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="93f84-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="93f84-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="93f84-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


