---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 1f9f0258bf107ae0ca7be7050f8db8e3db8b1ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705703"
---
# <span data-ttu-id="d20a6-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="d20a6-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="d20a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d20a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d20a6-103">Pobiera informacje o zaproszeniu do udziału danych.</span><span class="sxs-lookup"><span data-stu-id="d20a6-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="d20a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d20a6-104">SYNTAX</span></span>

### <span data-ttu-id="d20a6-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d20a6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d20a6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d20a6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d20a6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d20a6-107">DESCRIPTION</span></span>
<span data-ttu-id="d20a6-108">Polecenie cmdlet **Get-AzDataShareInvitation** pobiera informacje dotyczące zaproszeń dodanych w obszarze Udostępnianie danych.</span><span class="sxs-lookup"><span data-stu-id="d20a6-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="d20a6-109">Jeśli określisz nazwę zaproszenia, to polecenie cmdlet będzie pobierać informacje o zaproszeniu.</span><span class="sxs-lookup"><span data-stu-id="d20a6-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="d20a6-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich zaproszeniach w udziale.</span><span class="sxs-lookup"><span data-stu-id="d20a6-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="d20a6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d20a6-111">EXAMPLES</span></span>

### <span data-ttu-id="d20a6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d20a6-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="d20a6-113">Te polecenia dostarczają informacji na temat AdsInvitation zaproszeń w AdsShare udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="d20a6-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="d20a6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d20a6-114">PARAMETERS</span></span>

### <span data-ttu-id="d20a6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d20a6-115">-AccountName</span></span>
<span data-ttu-id="d20a6-116">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="d20a6-116">Azure data share account name</span></span>

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

### <span data-ttu-id="d20a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20a6-117">-DefaultProfile</span></span>
<span data-ttu-id="d20a6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d20a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d20a6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d20a6-119">-Name</span></span>
<span data-ttu-id="d20a6-120">Nazwa zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d20a6-120">Azure data share invitation name</span></span>

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

### <span data-ttu-id="d20a6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d20a6-121">-ResourceGroupName</span></span>
<span data-ttu-id="d20a6-122">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="d20a6-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d20a6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d20a6-123">-ResourceId</span></span>
<span data-ttu-id="d20a6-124">Identyfikator zasobu zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d20a6-124">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="d20a6-125">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="d20a6-125">-ShareName</span></span>
<span data-ttu-id="d20a6-126">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d20a6-126">Azure data share name</span></span>

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

### <span data-ttu-id="d20a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20a6-127">CommonParameters</span></span>
<span data-ttu-id="d20a6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d20a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20a6-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d20a6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20a6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d20a6-130">INPUTS</span></span>

### <span data-ttu-id="d20a6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d20a6-131">System.String</span></span>

## <span data-ttu-id="d20a6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d20a6-132">OUTPUTS</span></span>

### <span data-ttu-id="d20a6-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="d20a6-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="d20a6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d20a6-134">NOTES</span></span>

## <span data-ttu-id="d20a6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d20a6-135">RELATED LINKS</span></span>