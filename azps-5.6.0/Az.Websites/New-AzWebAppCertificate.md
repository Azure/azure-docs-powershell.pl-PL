---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 8e4ed309d4109ecfe230a522a65054213ae32049
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972337"
---
# <span data-ttu-id="0ebc0-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebc0-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="0ebc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ebc0-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebc0-103">Tworzy certyfikat zarządzany przez usługę aplikacji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="0ebc0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ebc0-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ebc0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ebc0-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebc0-106">Polecenie **cmdlet New-AzWebAppCertificate** tworzy certyfikat zarządzany usługi aplikacji Azure</span><span class="sxs-lookup"><span data-stu-id="0ebc0-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="0ebc0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ebc0-107">EXAMPLES</span></span>

### <span data-ttu-id="0ebc0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ebc0-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="0ebc0-109">To polecenie umożliwia utworzenie certyfikatu zarządzanego usługi aplikacji dla danej aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="0ebc0-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="0ebc0-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0ebc0-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="0ebc0-111">To polecenie tworzy certyfikat zarządzany przez usługę aplikacji i powiąza się z danym slotem aplikacji WebApp.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="0ebc0-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0ebc0-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="0ebc0-113">To polecenie tworzy certyfikat zarządzany przez usługę aplikacji i powiąza się z tą aplikacją WebApp.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="0ebc0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ebc0-114">PARAMETERS</span></span>

### <span data-ttu-id="0ebc0-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="0ebc0-115">-AddBinding</span></span>
<span data-ttu-id="0ebc0-116">Aby dodać utworzony certyfikat do witryny WebApp/slot.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-116">To add the created certificate to WebApp/slot.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebc0-117">-DefaultProfile</span></span>
<span data-ttu-id="0ebc0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebc0-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="0ebc0-119">-HostName</span></span>
<span data-ttu-id="0ebc0-120">Niestandardowe nazwy hostów skojarzone z aplikacją sieci Web/slotem.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0ebc0-121">-Name</span></span>
<span data-ttu-id="0ebc0-122">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebc0-123">-ResourceGroupName</span></span>
<span data-ttu-id="0ebc0-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-125">— Slot</span><span class="sxs-lookup"><span data-stu-id="0ebc0-125">-Slot</span></span>
<span data-ttu-id="0ebc0-126">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-126">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="0ebc0-127">-SslState</span></span>
<span data-ttu-id="0ebc0-128">Opcja stanu ssl.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-128">Ssl state option.</span></span>
<span data-ttu-id="0ebc0-129">Użyj albo "SniEnabled", albo "IpBasedEnabled".</span><span class="sxs-lookup"><span data-stu-id="0ebc0-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="0ebc0-130">Opcja domyślna to "SniEnabled".</span><span class="sxs-lookup"><span data-stu-id="0ebc0-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="0ebc0-131">-WebAppName</span></span>
<span data-ttu-id="0ebc0-132">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebc0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebc0-133">CommonParameters</span></span>
<span data-ttu-id="0ebc0-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebc0-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ebc0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebc0-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ebc0-136">INPUTS</span></span>

### <span data-ttu-id="0ebc0-137">Brak</span><span class="sxs-lookup"><span data-stu-id="0ebc0-137">None</span></span>

## <span data-ttu-id="0ebc0-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ebc0-138">OUTPUTS</span></span>

### <span data-ttu-id="0ebc0-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebc0-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="0ebc0-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ebc0-140">NOTES</span></span>

## <span data-ttu-id="0ebc0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ebc0-141">RELATED LINKS</span></span>
[<span data-ttu-id="0ebc0-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebc0-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)