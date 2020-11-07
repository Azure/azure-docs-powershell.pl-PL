---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705849"
---
# <span data-ttu-id="1dead-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1dead-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1dead-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dead-102">SYNOPSIS</span></span>
<span data-ttu-id="1dead-103">Sprawdza, czy jest konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1dead-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1dead-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dead-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dead-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1dead-105">DESCRIPTION</span></span>
<span data-ttu-id="1dead-106">Polecenie cmdlet **test-AzDataLakeAnalyticsAccount** sprawdza, czy istnieje konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1dead-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1dead-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dead-107">EXAMPLES</span></span>

### <span data-ttu-id="1dead-108">Przykład 1: Sprawdzanie, czy konto istnieje</span><span class="sxs-lookup"><span data-stu-id="1dead-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="1dead-109">To polecenie sprawdza, czy konto o nazwie ContosoAdlAccount istnieje.</span><span class="sxs-lookup"><span data-stu-id="1dead-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="1dead-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dead-110">PARAMETERS</span></span>

### <span data-ttu-id="1dead-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dead-111">-DefaultProfile</span></span>
<span data-ttu-id="1dead-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1dead-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dead-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1dead-113">-Name</span></span>
<span data-ttu-id="1dead-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1dead-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1dead-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dead-115">-ResourceGroupName</span></span>
<span data-ttu-id="1dead-116">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1dead-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="1dead-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dead-117">CommonParameters</span></span>
<span data-ttu-id="1dead-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dead-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dead-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dead-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dead-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dead-120">INPUTS</span></span>

### <span data-ttu-id="1dead-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1dead-121">System.String</span></span>

## <span data-ttu-id="1dead-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dead-122">OUTPUTS</span></span>

### <span data-ttu-id="1dead-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dead-123">System.Boolean</span></span>

## <span data-ttu-id="1dead-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dead-124">NOTES</span></span>

## <span data-ttu-id="1dead-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dead-125">RELATED LINKS</span></span>

[<span data-ttu-id="1dead-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1dead-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1dead-127">Nowe — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1dead-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1dead-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1dead-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


