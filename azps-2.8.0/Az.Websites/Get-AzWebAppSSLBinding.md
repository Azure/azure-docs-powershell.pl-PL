---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: a50716315796d46185b67099784bc550295231e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888501"
---
# <span data-ttu-id="40174-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="40174-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="40174-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40174-102">SYNOPSIS</span></span>
<span data-ttu-id="40174-103">Pobiera powiązanie SSL certyfikatu aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="40174-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="40174-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40174-104">SYNTAX</span></span>

### <span data-ttu-id="40174-105">S1</span><span class="sxs-lookup"><span data-stu-id="40174-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40174-106">S2</span><span class="sxs-lookup"><span data-stu-id="40174-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40174-107">Opis</span><span class="sxs-lookup"><span data-stu-id="40174-107">DESCRIPTION</span></span>
<span data-ttu-id="40174-108">Polecenie cmdlet **Get-AzWebAppSSLBinding** Pobiera powiązanie SSL (Secure Sockets Layer) dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="40174-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="40174-109">Powiązania SSL są używane do kojarzenia aplikacji sieci Web z przekazanym certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="40174-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="40174-110">Aplikacje sieci Web mogą być powiązane z wieloma certyfikatami.</span><span class="sxs-lookup"><span data-stu-id="40174-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="40174-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40174-111">EXAMPLES</span></span>

### <span data-ttu-id="40174-112">Przykład 1: uzyskiwanie powiązań SSL dla aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="40174-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="40174-113">To polecenie pobiera powiązania protokołu SSL dla aplikacji sieci Web ContosoWebApp, która jest skojarzona z grupą zasobów ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="40174-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="40174-114">Przykład 2: używanie odwołania do obiektu w celu uzyskania powiązań SSL dla aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="40174-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="40174-115">Polecenia w tym przykładzie uzyskują również powiązania SSL dla aplikacji sieci Web ContosoWebApp; Jednak w tym przypadku zamiast nazwy aplikacji sieci Web i nazwy skojarzonej grupy zasobów zostanie użyte odwołanie do obiektu.</span><span class="sxs-lookup"><span data-stu-id="40174-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="40174-116">To odwołanie do obiektu jest tworzone przez pierwsze polecenie w przykładzie, w którym użyto polecenia **Get-AzWebApp** w celu utworzenia odwołania do obiektu do aplikacji sieci Web o nazwie ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="40174-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="40174-117">Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.</span><span class="sxs-lookup"><span data-stu-id="40174-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="40174-118">Ta zmienna i polecenie cmdlet **Get-AzWebAppSSLBinding** są następnie używane przez drugie polecenie w celu uzyskania powiązań SSL.</span><span class="sxs-lookup"><span data-stu-id="40174-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="40174-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40174-119">PARAMETERS</span></span>

### <span data-ttu-id="40174-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40174-120">-DefaultProfile</span></span>
<span data-ttu-id="40174-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40174-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40174-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40174-122">-Name</span></span>
<span data-ttu-id="40174-123">Określa nazwę powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="40174-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40174-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40174-124">-ResourceGroupName</span></span>
<span data-ttu-id="40174-125">Określa nazwę grupy zasobów, do której przypisano certyfikat.</span><span class="sxs-lookup"><span data-stu-id="40174-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="40174-126">Nie można użyć parametru *ResourceGroupName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="40174-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40174-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="40174-127">-Slot</span></span>
<span data-ttu-id="40174-128">Określa miejsce wdrożenia aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="40174-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="40174-129">Aby uzyskać miejsce do wdrożenia, użyj polecenia cmdlet Get-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="40174-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40174-130">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="40174-130">-WebApp</span></span>
<span data-ttu-id="40174-131">Określa aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="40174-131">Specifies a Web App.</span></span>
<span data-ttu-id="40174-132">Aby uzyskać aplikację sieci Web, użyj polecenia cmdlet Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="40174-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40174-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="40174-133">-WebAppName</span></span>
<span data-ttu-id="40174-134">Określa nazwę aplikacji sieci Web, z której to polecenie cmdlet pobiera powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="40174-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="40174-135">Nie można użyć parametru *WebAppName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="40174-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40174-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40174-136">CommonParameters</span></span>
<span data-ttu-id="40174-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40174-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40174-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40174-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40174-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40174-139">INPUTS</span></span>

### <span data-ttu-id="40174-140">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="40174-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="40174-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40174-141">OUTPUTS</span></span>

### <span data-ttu-id="40174-142">Microsoft. Azure. Management. Web. MODELES. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="40174-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="40174-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40174-143">NOTES</span></span>

## <span data-ttu-id="40174-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40174-144">RELATED LINKS</span></span>

[<span data-ttu-id="40174-145">Nowe — AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="40174-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="40174-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="40174-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="40174-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40174-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


