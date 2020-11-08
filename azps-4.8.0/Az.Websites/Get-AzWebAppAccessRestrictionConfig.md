---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222406"
---
# <span data-ttu-id="964a3-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="964a3-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="964a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="964a3-102">SYNOPSIS</span></span>
<span data-ttu-id="964a3-103">Pobiera konfigurację restiction programu Access dla aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="964a3-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="964a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="964a3-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="964a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="964a3-105">DESCRIPTION</span></span>
<span data-ttu-id="964a3-106">Polecenie cmdlet **Get-AzWebAppAccessRestrictionConfig** Pobiera konfigurację ograniczeń dostępu na temat aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="964a3-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="964a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="964a3-107">EXAMPLES</span></span>

### <span data-ttu-id="964a3-108">Przykład 1: Uzyskiwanie konfiguracji ograniczeń dostępu do aplikacji sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="964a3-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="964a3-109">To polecenie pobiera konfigurację ograniczeń dostępu aplikacji sieci Web o nazwie ContosoSite należącej do pozycji domyślne grupy zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="964a3-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="964a3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="964a3-110">PARAMETERS</span></span>

### <span data-ttu-id="964a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964a3-111">-DefaultProfile</span></span>
<span data-ttu-id="964a3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="964a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="964a3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="964a3-113">-Name</span></span>
<span data-ttu-id="964a3-114">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="964a3-114">WebApp Name</span></span>

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

### <span data-ttu-id="964a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="964a3-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="964a3-116">Resource Group Name</span></span>

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

### <span data-ttu-id="964a3-117">-Slotname</span><span class="sxs-lookup"><span data-stu-id="964a3-117">-SlotName</span></span>
<span data-ttu-id="964a3-118">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="964a3-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="964a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964a3-119">CommonParameters</span></span>
<span data-ttu-id="964a3-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="964a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964a3-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="964a3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964a3-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="964a3-122">INPUTS</span></span>

### <span data-ttu-id="964a3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="964a3-123">System.String</span></span>

## <span data-ttu-id="964a3-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="964a3-124">OUTPUTS</span></span>

### <span data-ttu-id="964a3-125">Microsoft. Azure. Commands. webapps. modele. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="964a3-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="964a3-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="964a3-126">NOTES</span></span>

## <span data-ttu-id="964a3-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="964a3-127">RELATED LINKS</span></span>

[<span data-ttu-id="964a3-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="964a3-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="964a3-129">Dodaj-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="964a3-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="964a3-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="964a3-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
