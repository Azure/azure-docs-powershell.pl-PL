---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 443f69bc507cb0c9d5fe4c1b59cb3ef8e6e46803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963057"
---
# <span data-ttu-id="eb926-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="eb926-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="eb926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb926-102">SYNOPSIS</span></span>
<span data-ttu-id="eb926-103">Otrzymuje zaproszenie do udostępniania danych z informacjami.</span><span class="sxs-lookup"><span data-stu-id="eb926-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="eb926-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eb926-104">SYNTAX</span></span>

### <span data-ttu-id="eb926-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="eb926-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb926-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb926-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb926-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="eb926-107">DESCRIPTION</span></span>
<span data-ttu-id="eb926-108">Polecenie **cmdlet Get-AzDataShareInvitation** pobiera informacje o zaproszeniach dodanych do udziału danych.</span><span class="sxs-lookup"><span data-stu-id="eb926-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="eb926-109">Jeśli określisz nazwę zaproszenia, to polecenie cmdlet otrzyma informacje o zaproszeniu.</span><span class="sxs-lookup"><span data-stu-id="eb926-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="eb926-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich zaproszeniach w udziału.</span><span class="sxs-lookup"><span data-stu-id="eb926-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="eb926-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eb926-111">EXAMPLES</span></span>

### <span data-ttu-id="eb926-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb926-112">Example 1</span></span>
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

<span data-ttu-id="eb926-113">To polecenia zawierają informacje na temat zaproszenia do prezentowania zaproszenia w użytce danych w użytości AdsShare.</span><span class="sxs-lookup"><span data-stu-id="eb926-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="eb926-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb926-114">PARAMETERS</span></span>

### <span data-ttu-id="eb926-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb926-115">-AccountName</span></span>
<span data-ttu-id="eb926-116">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eb926-116">Azure data share account name</span></span>

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

### <span data-ttu-id="eb926-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb926-117">-DefaultProfile</span></span>
<span data-ttu-id="eb926-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb926-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb926-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eb926-119">-Name</span></span>
<span data-ttu-id="eb926-120">Nazwa zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eb926-120">Azure data share invitation name</span></span>

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

### <span data-ttu-id="eb926-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb926-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb926-122">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eb926-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eb926-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb926-123">-ResourceId</span></span>
<span data-ttu-id="eb926-124">Identyfikator zasobu zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eb926-124">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="eb926-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="eb926-125">-ShareName</span></span>
<span data-ttu-id="eb926-126">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eb926-126">Azure data share name</span></span>

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

### <span data-ttu-id="eb926-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb926-127">CommonParameters</span></span>
<span data-ttu-id="eb926-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb926-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb926-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb926-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb926-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb926-130">INPUTS</span></span>

### <span data-ttu-id="eb926-131">System.String</span><span class="sxs-lookup"><span data-stu-id="eb926-131">System.String</span></span>

## <span data-ttu-id="eb926-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb926-132">OUTPUTS</span></span>

### <span data-ttu-id="eb926-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="eb926-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="eb926-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eb926-134">NOTES</span></span>

## <span data-ttu-id="eb926-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb926-135">RELATED LINKS</span></span>
