---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4f3ffda3bbac6658cf54af1c7b459ce70f651e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719333"
---
# <span data-ttu-id="92d6c-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="92d6c-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="92d6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="92d6c-103">Sprawdza, czy jest konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="92d6c-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92d6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92d6c-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="92d6c-106">Polecenie cmdlet **test-AzureRmDataLakeAnalyticsAccount** sprawdza, czy istnieje konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="92d6c-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="92d6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="92d6c-108">Przykład 1: Sprawdzanie, czy konto istnieje</span><span class="sxs-lookup"><span data-stu-id="92d6c-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="92d6c-109">To polecenie sprawdza, czy konto o nazwie ContosoAdlAccount istnieje.</span><span class="sxs-lookup"><span data-stu-id="92d6c-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="92d6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="92d6c-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92d6c-111">-Name</span></span>
<span data-ttu-id="92d6c-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="92d6c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="92d6c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d6c-113">-ResourceGroupName</span></span>
<span data-ttu-id="92d6c-114">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="92d6c-114">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="92d6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d6c-115">-DefaultProfile</span></span>
<span data-ttu-id="92d6c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92d6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92d6c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d6c-117">CommonParameters</span></span>
<span data-ttu-id="92d6c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d6c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d6c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d6c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d6c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92d6c-120">INPUTS</span></span>

## <span data-ttu-id="92d6c-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92d6c-121">OUTPUTS</span></span>

### <span data-ttu-id="92d6c-122">logiczną</span><span class="sxs-lookup"><span data-stu-id="92d6c-122">bool</span></span>
<span data-ttu-id="92d6c-123">Prawda lub FAŁSZ wskazujący, czy konto istnieje, czy nie.</span><span class="sxs-lookup"><span data-stu-id="92d6c-123">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="92d6c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92d6c-124">NOTES</span></span>

## <span data-ttu-id="92d6c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92d6c-125">RELATED LINKS</span></span>

[<span data-ttu-id="92d6c-126">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="92d6c-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="92d6c-127">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="92d6c-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="92d6c-128">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="92d6c-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


