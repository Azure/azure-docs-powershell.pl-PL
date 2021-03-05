---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 7c443625294b3a23ac79dfcbabb724a2d3fceaa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971745"
---
# <span data-ttu-id="7371c-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="7371c-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="7371c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7371c-102">SYNOPSIS</span></span>
<span data-ttu-id="7371c-103">Uzyskiwanie ustawień zabezpieczeń w Centrum zabezpieczeń Azure</span><span class="sxs-lookup"><span data-stu-id="7371c-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="7371c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7371c-104">SYNTAX</span></span>

### <span data-ttu-id="7371c-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7371c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7371c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7371c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7371c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7371c-107">DESCRIPTION</span></span>
<span data-ttu-id="7371c-108">Polecenie Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="7371c-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="7371c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7371c-109">EXAMPLES</span></span>

### <span data-ttu-id="7371c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7371c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="7371c-111">Pobiera ustawienie eksportu danych MCAS</span><span class="sxs-lookup"><span data-stu-id="7371c-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="7371c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7371c-112">PARAMETERS</span></span>

### <span data-ttu-id="7371c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7371c-113">-DefaultProfile</span></span>
<span data-ttu-id="7371c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7371c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7371c-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="7371c-115">-SettingName</span></span>
<span data-ttu-id="7371c-116">Nazwa ustawienia.</span><span class="sxs-lookup"><span data-stu-id="7371c-116">Setting name.</span></span> <span data-ttu-id="7371c-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="7371c-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7371c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7371c-118">CommonParameters</span></span>
<span data-ttu-id="7371c-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7371c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7371c-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7371c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7371c-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7371c-121">INPUTS</span></span>

### <span data-ttu-id="7371c-122">System.String</span><span class="sxs-lookup"><span data-stu-id="7371c-122">System.String</span></span>

## <span data-ttu-id="7371c-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7371c-123">OUTPUTS</span></span>

### <span data-ttu-id="7371c-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="7371c-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="7371c-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="7371c-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="7371c-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7371c-126">NOTES</span></span>

## <span data-ttu-id="7371c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7371c-127">RELATED LINKS</span></span>
