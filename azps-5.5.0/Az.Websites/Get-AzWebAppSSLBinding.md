---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241555"
---
# <span data-ttu-id="ba348-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ba348-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="ba348-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba348-102">SYNOPSIS</span></span>
<span data-ttu-id="ba348-103">Pobiera powiązanie SSL certyfikatu aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ba348-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="ba348-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba348-104">SYNTAX</span></span>

### <span data-ttu-id="ba348-105">S1</span><span class="sxs-lookup"><span data-stu-id="ba348-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba348-106">S2</span><span class="sxs-lookup"><span data-stu-id="ba348-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba348-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba348-107">DESCRIPTION</span></span>
<span data-ttu-id="ba348-108">Polecenie **cmdlet Get-AzWebAppSSLBinding** pobiera powiązanie Secure Sockets Layer (SSL) dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ba348-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="ba348-109">Powiązania SSL służą do kojarzenia aplikacji Sieci Web z przekazanym certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="ba348-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="ba348-110">Aplikacje Sieci Web mogą być powiązane z wieloma certyfikatami.</span><span class="sxs-lookup"><span data-stu-id="ba348-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="ba348-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba348-111">EXAMPLES</span></span>

### <span data-ttu-id="ba348-112">Przykład 1. Uzyskiwanie powiązań SSL dla aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="ba348-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="ba348-113">To polecenie pobiera powiązania SSL dla aplikacji Sieci Web ContosoWebApp, która jest skojarzona z grupą zasobów ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba348-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="ba348-114">Przykład 2. Uzyskiwanie powiązań SSL dla aplikacji sieci Web za pomocą odwołania do obiektu</span><span class="sxs-lookup"><span data-stu-id="ba348-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="ba348-115">Polecenia w tym przykładzie również uzyskają powiązania SSL dla aplikacji sieci Web ContosoWebApp; Jednak w tym przypadku zamiast nazwy aplikacji Web App i nazwy skojarzonej grupy zasobów jest używane odwołanie do obiektu.</span><span class="sxs-lookup"><span data-stu-id="ba348-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="ba348-116">To odwołanie do obiektu jest tworzone za pomocą pierwszego polecenia w tym przykładzie, które używa aplikacji **Get-AzWebApp** do utworzenia odwołania do obiektu do aplikacji Sieci Web o nazwie ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="ba348-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="ba348-117">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.</span><span class="sxs-lookup"><span data-stu-id="ba348-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="ba348-118">Ta zmienna i polecenie cmdlet **Get-AzWebAppSSLBinding** są następnie używane przez drugie polecenie do uzyskania powiązań SSL.</span><span class="sxs-lookup"><span data-stu-id="ba348-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="ba348-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba348-119">PARAMETERS</span></span>

### <span data-ttu-id="ba348-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba348-120">-DefaultProfile</span></span>
<span data-ttu-id="ba348-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba348-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba348-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ba348-122">-Name</span></span>
<span data-ttu-id="ba348-123">Określa nazwę powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="ba348-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="ba348-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba348-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba348-125">Określa nazwę grupy zasobów, do których jest przypisany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="ba348-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="ba348-126">W tym samym *poleceniu nie można* użyć parametru ResourceGroupName ani *parametru WebApp.*</span><span class="sxs-lookup"><span data-stu-id="ba348-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="ba348-127">— Slot</span><span class="sxs-lookup"><span data-stu-id="ba348-127">-Slot</span></span>
<span data-ttu-id="ba348-128">Określa miejsce wdrożenia aplikacji Sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ba348-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="ba348-129">Aby uzyskać miejsce wdrożenia, użyj Get-AzWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba348-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="ba348-130">— WebApp</span><span class="sxs-lookup"><span data-stu-id="ba348-130">-WebApp</span></span>
<span data-ttu-id="ba348-131">Określa aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ba348-131">Specifies a Web App.</span></span>
<span data-ttu-id="ba348-132">Aby uzyskać aplikację Sieci Web, użyj Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba348-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="ba348-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="ba348-133">-WebAppName</span></span>
<span data-ttu-id="ba348-134">Określa nazwę aplikacji Sieci Web, z których to polecenie cmdlet pobiera powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="ba348-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="ba348-135">W tym samym poleceniu nie można użyć parametru *WebAppName* ani parametru *WebApp.*</span><span class="sxs-lookup"><span data-stu-id="ba348-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="ba348-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba348-136">CommonParameters</span></span>
<span data-ttu-id="ba348-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba348-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba348-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba348-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba348-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba348-139">INPUTS</span></span>

### <span data-ttu-id="ba348-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ba348-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ba348-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba348-141">OUTPUTS</span></span>

### <span data-ttu-id="ba348-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="ba348-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="ba348-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba348-143">NOTES</span></span>

## <span data-ttu-id="ba348-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba348-144">RELATED LINKS</span></span>

[<span data-ttu-id="ba348-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ba348-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="ba348-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ba348-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="ba348-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba348-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


