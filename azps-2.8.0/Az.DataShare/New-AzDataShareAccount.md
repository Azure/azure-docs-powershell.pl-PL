---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: c0b2b8eb249e466c0e57127e0df9ee9b0afad048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705677"
---
# <span data-ttu-id="f05ec-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f05ec-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="f05ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f05ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f05ec-103">Tworzy nowe konto udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="f05ec-103">Creates new data share account</span></span>

## <span data-ttu-id="f05ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f05ec-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f05ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f05ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f05ec-106">Polecenie cmdlet **New-AzDataShareAccount** tworzy konto dataudział w określonej grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f05ec-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="f05ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f05ec-107">EXAMPLES</span></span>

### <span data-ttu-id="f05ec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f05ec-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="f05ec-109">Tworzy konto o nazwie "WikiADS" w grupie zasobów "ADS"</span><span class="sxs-lookup"><span data-stu-id="f05ec-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="f05ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f05ec-110">PARAMETERS</span></span>

### <span data-ttu-id="f05ec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f05ec-111">-AsJob</span></span>
<span data-ttu-id="f05ec-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="f05ec-112">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05ec-113">-DefaultProfile</span></span>
<span data-ttu-id="f05ec-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f05ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05ec-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f05ec-115">-Location</span></span>
<span data-ttu-id="f05ec-116">Lokalizacja, w której ma zostać utworzone konto udziału danych.</span><span class="sxs-lookup"><span data-stu-id="f05ec-116">The location in which to create the data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05ec-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f05ec-117">-Name</span></span>
<span data-ttu-id="f05ec-118">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="f05ec-118">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="f05ec-120">Zostanie utworzona nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="f05ec-120">The resource group name of the azure data share account will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05ec-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="f05ec-121">-Tag</span></span>
<span data-ttu-id="f05ec-122">Znaczniki, które mają zostać skojarzone z kontem usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="f05ec-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05ec-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f05ec-123">-Confirm</span></span>
<span data-ttu-id="f05ec-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f05ec-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05ec-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f05ec-125">-WhatIf</span></span>
<span data-ttu-id="f05ec-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f05ec-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f05ec-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f05ec-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05ec-128">CommonParameters</span></span>
<span data-ttu-id="f05ec-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f05ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05ec-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05ec-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05ec-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f05ec-131">INPUTS</span></span>

### <span data-ttu-id="f05ec-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f05ec-132">None</span></span>

## <span data-ttu-id="f05ec-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f05ec-133">OUTPUTS</span></span>

### <span data-ttu-id="f05ec-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f05ec-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="f05ec-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f05ec-135">NOTES</span></span>

## <span data-ttu-id="f05ec-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f05ec-136">RELATED LINKS</span></span>
