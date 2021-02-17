---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186122"
---
# <span data-ttu-id="8c9b8-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="8c9b8-101">Get-AzDataShare</span></span>

## <span data-ttu-id="8c9b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9b8-103">Uzyskaj informacje na temat udziałów danych.</span><span class="sxs-lookup"><span data-stu-id="8c9b8-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="8c9b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c9b8-104">SYNTAX</span></span>

### <span data-ttu-id="8c9b8-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8c9b8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c9b8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c9b8-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c9b8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c9b8-107">DESCRIPTION</span></span>
<span data-ttu-id="8c9b8-108">Polecenie **cmdlet Get-AzDataShare** pobiera informacje o udziałach danych w usłudze azure data share accoount.</span><span class="sxs-lookup"><span data-stu-id="8c9b8-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="8c9b8-109">Jeśli określisz nazwę udziału danych, to polecenie cmdlet pobiera informacje o tym udostępnie danych.</span><span class="sxs-lookup"><span data-stu-id="8c9b8-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="8c9b8-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich udziałach danych w koncie udostępniania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8c9b8-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="8c9b8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c9b8-111">EXAMPLES</span></span>

### <span data-ttu-id="8c9b8-112">Przykład 1. Uzyskiwanie określonego udziału danych</span><span class="sxs-lookup"><span data-stu-id="8c9b8-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="8c9b8-113">To polecenie służy do wyświetlania informacji o udostępnianiu danych usługi AdsShare na koncie współużytkowania danych platformy Azure WikiAdsAccount i usłudze ADS grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c9b8-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="8c9b8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c9b8-114">PARAMETERS</span></span>

### <span data-ttu-id="8c9b8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c9b8-115">-AccountName</span></span>
<span data-ttu-id="8c9b8-116">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8c9b8-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9b8-117">-DefaultProfile</span></span>
<span data-ttu-id="8c9b8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c9b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c9b8-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c9b8-119">-Name</span></span>
<span data-ttu-id="8c9b8-120">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8c9b8-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c9b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c9b8-122">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="8c9b8-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c9b8-123">-ResourceId</span></span>
<span data-ttu-id="8c9b8-124">Identyfikator zasobu udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8c9b8-124">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9b8-125">CommonParameters</span></span>
<span data-ttu-id="8c9b8-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c9b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9b8-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c9b8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9b8-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c9b8-128">INPUTS</span></span>

### <span data-ttu-id="8c9b8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8c9b8-129">System.String</span></span>

## <span data-ttu-id="8c9b8-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c9b8-130">OUTPUTS</span></span>

### <span data-ttu-id="8c9b8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8c9b8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8c9b8-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c9b8-132">NOTES</span></span>

## <span data-ttu-id="8c9b8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c9b8-133">RELATED LINKS</span></span>
