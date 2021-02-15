---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 56f8d69325e5a7918668ac2807449f348e73c91b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182450"
---
# <span data-ttu-id="a2d45-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a2d45-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="a2d45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d45-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d45-103">Tworzy certyfikat zarządzany przez usługę aplikacji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a2d45-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="a2d45-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a2d45-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2d45-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a2d45-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d45-106">Polecenie **cmdlet New-AzWebAppCertificate** tworzy certyfikat zarządzany usługi aplikacji Azure</span><span class="sxs-lookup"><span data-stu-id="a2d45-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="a2d45-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a2d45-107">EXAMPLES</span></span>

### <span data-ttu-id="a2d45-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2d45-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="a2d45-109">To polecenie umożliwia utworzenie certyfikatu zarządzanego usługi aplikacji dla danej aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="a2d45-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="a2d45-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2d45-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="a2d45-111">To polecenie tworzy certyfikat zarządzany przez usługę aplikacji i powiąza się z danym slotem aplikacji WebApp.</span><span class="sxs-lookup"><span data-stu-id="a2d45-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="a2d45-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a2d45-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="a2d45-113">To polecenie tworzy certyfikat zarządzany przez usługę aplikacji i powiąza się z tą aplikacją WebApp.</span><span class="sxs-lookup"><span data-stu-id="a2d45-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="a2d45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2d45-114">PARAMETERS</span></span>

### <span data-ttu-id="a2d45-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="a2d45-115">-AddBinding</span></span>
<span data-ttu-id="a2d45-116">Aby dodać utworzony certyfikat do aplikacji WebApp/slot.</span><span class="sxs-lookup"><span data-stu-id="a2d45-116">To add the created certificate to WebApp/slot.</span></span>

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

### <span data-ttu-id="a2d45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d45-117">-DefaultProfile</span></span>
<span data-ttu-id="a2d45-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d45-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="a2d45-119">-HostName</span></span>
<span data-ttu-id="a2d45-120">Niestandardowe nazwy hostów skojarzone z aplikacją sieci Web/slotem.</span><span class="sxs-lookup"><span data-stu-id="a2d45-120">Custom hostnames associated with web app/slot.</span></span>

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

### <span data-ttu-id="a2d45-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a2d45-121">-Name</span></span>
<span data-ttu-id="a2d45-122">Nazwa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a2d45-122">The name of the certificate.</span></span>

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

### <span data-ttu-id="a2d45-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d45-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2d45-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a2d45-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2d45-125">— Slot</span><span class="sxs-lookup"><span data-stu-id="a2d45-125">-Slot</span></span>
<span data-ttu-id="a2d45-126">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a2d45-126">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a2d45-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="a2d45-127">-SslState</span></span>
<span data-ttu-id="a2d45-128">Opcja stanu ssl.</span><span class="sxs-lookup"><span data-stu-id="a2d45-128">Ssl state option.</span></span>
<span data-ttu-id="a2d45-129">Użyj albo "SniEnabled", albo "IpBasedEnabled".</span><span class="sxs-lookup"><span data-stu-id="a2d45-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="a2d45-130">Opcja domyślna to "SniEnabled".</span><span class="sxs-lookup"><span data-stu-id="a2d45-130">Default option is 'SniEnabled'.</span></span>

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

### <span data-ttu-id="a2d45-131">- WebAppName</span><span class="sxs-lookup"><span data-stu-id="a2d45-131">-WebAppName</span></span>
<span data-ttu-id="a2d45-132">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a2d45-132">The name of the web app.</span></span>

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

### <span data-ttu-id="a2d45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d45-133">CommonParameters</span></span>
<span data-ttu-id="a2d45-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d45-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2d45-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d45-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2d45-136">INPUTS</span></span>

### <span data-ttu-id="a2d45-137">Brak</span><span class="sxs-lookup"><span data-stu-id="a2d45-137">None</span></span>

## <span data-ttu-id="a2d45-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2d45-138">OUTPUTS</span></span>

### <span data-ttu-id="a2d45-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="a2d45-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="a2d45-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a2d45-140">NOTES</span></span>

## <span data-ttu-id="a2d45-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2d45-141">RELATED LINKS</span></span>
[<span data-ttu-id="a2d45-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a2d45-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)