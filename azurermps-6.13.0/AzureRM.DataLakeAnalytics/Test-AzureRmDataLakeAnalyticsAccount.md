---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: e527501424edfbbc12693b47b5858c3c46592402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717431"
---
# <span data-ttu-id="a7347-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a7347-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a7347-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7347-102">SYNOPSIS</span></span>
<span data-ttu-id="a7347-103">Sprawdza, czy jest konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a7347-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7347-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7347-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7347-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7347-105">DESCRIPTION</span></span>
<span data-ttu-id="a7347-106">Polecenie cmdlet **test-AzureRmDataLakeAnalyticsAccount** sprawdza, czy istnieje konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a7347-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a7347-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7347-107">EXAMPLES</span></span>

### <span data-ttu-id="a7347-108">Przykład 1: Sprawdzanie, czy konto istnieje</span><span class="sxs-lookup"><span data-stu-id="a7347-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="a7347-109">To polecenie sprawdza, czy konto o nazwie ContosoAdlAccount istnieje.</span><span class="sxs-lookup"><span data-stu-id="a7347-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="a7347-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7347-110">PARAMETERS</span></span>

### <span data-ttu-id="a7347-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7347-111">-DefaultProfile</span></span>
<span data-ttu-id="a7347-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a7347-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7347-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7347-113">-Name</span></span>
<span data-ttu-id="a7347-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a7347-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a7347-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7347-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7347-116">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a7347-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a7347-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7347-117">CommonParameters</span></span>
<span data-ttu-id="a7347-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7347-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7347-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7347-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7347-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7347-120">INPUTS</span></span>

### <span data-ttu-id="a7347-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a7347-121">System.String</span></span>

## <span data-ttu-id="a7347-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7347-122">OUTPUTS</span></span>

### <span data-ttu-id="a7347-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7347-123">System.Boolean</span></span>

## <span data-ttu-id="a7347-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7347-124">NOTES</span></span>

## <span data-ttu-id="a7347-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7347-125">RELATED LINKS</span></span>

[<span data-ttu-id="a7347-126">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a7347-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a7347-127">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a7347-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a7347-128">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a7347-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


