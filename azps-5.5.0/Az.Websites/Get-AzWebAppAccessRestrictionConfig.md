---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182466"
---
# <span data-ttu-id="b3e03-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b3e03-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="b3e03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e03-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e03-103">Pobiera konfigurację usługi Restiction programu Access dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b3e03-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="b3e03-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3e03-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3e03-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3e03-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e03-106">Polecenie **cmdlet Get-AzWebAppAccessRestrictionConfig** pobiera konfigurację ograniczeń dostępu dotyczących aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b3e03-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="b3e03-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3e03-107">EXAMPLES</span></span>

### <span data-ttu-id="b3e03-108">Przykład 1. Uzyskiwanie konfiguracji ograniczeń dostępu aplikacji sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b3e03-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b3e03-109">To polecenie pobiera konfigurację ograniczeń dostępu aplikacji Sieci Web o nazwie ContosoSite, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b3e03-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b3e03-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3e03-110">PARAMETERS</span></span>

### <span data-ttu-id="b3e03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e03-111">-DefaultProfile</span></span>
<span data-ttu-id="b3e03-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e03-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3e03-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b3e03-113">-Name</span></span>
<span data-ttu-id="b3e03-114">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="b3e03-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e03-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e03-115">-ResourceGroupName</span></span>
<span data-ttu-id="b3e03-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b3e03-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b3e03-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="b3e03-117">-SlotName</span></span>
<span data-ttu-id="b3e03-118">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b3e03-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e03-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e03-119">CommonParameters</span></span>
<span data-ttu-id="b3e03-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e03-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e03-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3e03-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e03-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e03-122">INPUTS</span></span>

### <span data-ttu-id="b3e03-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b3e03-123">System.String</span></span>

## <span data-ttu-id="b3e03-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3e03-124">OUTPUTS</span></span>

### <span data-ttu-id="b3e03-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b3e03-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="b3e03-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3e03-126">NOTES</span></span>

## <span data-ttu-id="b3e03-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3e03-127">RELATED LINKS</span></span>

[<span data-ttu-id="b3e03-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b3e03-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="b3e03-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b3e03-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="b3e03-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b3e03-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
