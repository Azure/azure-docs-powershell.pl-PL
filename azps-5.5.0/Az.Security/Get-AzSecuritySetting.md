---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189138"
---
# <span data-ttu-id="52ba5-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="52ba5-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="52ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="52ba5-103">Uzyskiwanie ustawień zabezpieczeń w Centrum zabezpieczeń Azure</span><span class="sxs-lookup"><span data-stu-id="52ba5-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="52ba5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52ba5-104">SYNTAX</span></span>

### <span data-ttu-id="52ba5-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="52ba5-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52ba5-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="52ba5-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52ba5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="52ba5-107">DESCRIPTION</span></span>
<span data-ttu-id="52ba5-108">Polecenie Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="52ba5-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="52ba5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52ba5-109">EXAMPLES</span></span>

### <span data-ttu-id="52ba5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52ba5-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="52ba5-111">Pobiera ustawienie eksportu danych MCAS</span><span class="sxs-lookup"><span data-stu-id="52ba5-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="52ba5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52ba5-112">PARAMETERS</span></span>

### <span data-ttu-id="52ba5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ba5-113">-DefaultProfile</span></span>
<span data-ttu-id="52ba5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52ba5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ba5-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="52ba5-115">-SettingName</span></span>
<span data-ttu-id="52ba5-116">Nazwa ustawienia.</span><span class="sxs-lookup"><span data-stu-id="52ba5-116">Setting name.</span></span> <span data-ttu-id="52ba5-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="52ba5-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="52ba5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ba5-118">CommonParameters</span></span>
<span data-ttu-id="52ba5-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ba5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ba5-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52ba5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ba5-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52ba5-121">INPUTS</span></span>

### <span data-ttu-id="52ba5-122">System.String</span><span class="sxs-lookup"><span data-stu-id="52ba5-122">System.String</span></span>

## <span data-ttu-id="52ba5-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52ba5-123">OUTPUTS</span></span>

### <span data-ttu-id="52ba5-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="52ba5-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="52ba5-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="52ba5-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="52ba5-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52ba5-126">NOTES</span></span>

## <span data-ttu-id="52ba5-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52ba5-127">RELATED LINKS</span></span>
