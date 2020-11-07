---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 2b3eda3aadca93415d93154a9a70361c789c94ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894597"
---
# <span data-ttu-id="ac9a1-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="ac9a1-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="ac9a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9a1-103">Tworzy nowe konto udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="ac9a1-103">Creates new data share account</span></span>

## <span data-ttu-id="ac9a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac9a1-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac9a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9a1-106">Polecenie cmdlet **New-AzDataShareAccount** tworzy konto dataudział w określonej grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="ac9a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9a1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ac9a1-108">Example 1</span></span>
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

<span data-ttu-id="ac9a1-109">Tworzy konto o nazwie "WikiADS" w grupie zasobów "ADS"</span><span class="sxs-lookup"><span data-stu-id="ac9a1-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="ac9a1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac9a1-110">PARAMETERS</span></span>

### <span data-ttu-id="ac9a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac9a1-111">-AsJob</span></span>
<span data-ttu-id="ac9a1-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="ac9a1-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="ac9a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9a1-113">-DefaultProfile</span></span>
<span data-ttu-id="ac9a1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9a1-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ac9a1-115">-Location</span></span>
<span data-ttu-id="ac9a1-116">Lokalizacja, w której ma zostać utworzone konto udziału danych.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="ac9a1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac9a1-117">-Name</span></span>
<span data-ttu-id="ac9a1-118">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="ac9a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac9a1-120">Zostanie utworzona nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="ac9a1-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac9a1-121">-Tag</span></span>
<span data-ttu-id="ac9a1-122">Znaczniki, które mają zostać skojarzone z kontem usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-122">The tags to associate with the azure data share account.</span></span>

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

### <span data-ttu-id="ac9a1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac9a1-123">-Confirm</span></span>
<span data-ttu-id="ac9a1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac9a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac9a1-125">-WhatIf</span></span>
<span data-ttu-id="ac9a1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac9a1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac9a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9a1-128">CommonParameters</span></span>
<span data-ttu-id="ac9a1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9a1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9a1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9a1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac9a1-131">INPUTS</span></span>

### <span data-ttu-id="ac9a1-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ac9a1-132">None</span></span>

## <span data-ttu-id="ac9a1-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac9a1-133">OUTPUTS</span></span>

### <span data-ttu-id="ac9a1-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="ac9a1-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="ac9a1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac9a1-135">NOTES</span></span>

## <span data-ttu-id="ac9a1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac9a1-136">RELATED LINKS</span></span>
