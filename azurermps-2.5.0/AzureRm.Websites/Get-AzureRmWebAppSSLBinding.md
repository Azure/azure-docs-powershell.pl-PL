---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 103c5e75b433fcb585113e8ef6bc89aab1f82d7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897761"
---
# <span data-ttu-id="9cfd4-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9cfd4-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="9cfd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cfd4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfd4-103">Pobiera powiązanie SSL certyfikatu aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cfd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cfd4-104">SYNTAX</span></span>

### <span data-ttu-id="9cfd4-105">S1</span><span class="sxs-lookup"><span data-stu-id="9cfd4-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cfd4-106">S2</span><span class="sxs-lookup"><span data-stu-id="9cfd4-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cfd4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9cfd4-107">DESCRIPTION</span></span>
<span data-ttu-id="9cfd4-108">Polecenie cmdlet **Get-AzureRmWebAppSSLBinding** Pobiera powiązanie SSL (Secure Sockets Layer) dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="9cfd4-109">Powiązania SSL są używane do kojarzenia aplikacji sieci Web z przekazanym certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="9cfd4-110">Aplikacje sieci Web mogą być powiązane z wieloma certyfikatami.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="9cfd4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cfd4-111">EXAMPLES</span></span>

### <span data-ttu-id="9cfd4-112">Przykład 1: uzyskiwanie powiązań SSL dla aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="9cfd4-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="9cfd4-113">To polecenie pobiera powiązania protokołu SSL dla aplikacji sieci Web ContosoWebApp, która jest skojarzona z grupą zasobów ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="9cfd4-114">Przykład 2: używanie odwołania do obiektu w celu uzyskania powiązań SSL dla aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="9cfd4-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="9cfd4-115">Polecenia w tym przykładzie uzyskują również powiązania SSL dla aplikacji sieci Web ContosoWebApp; Jednak w tym przypadku zamiast nazwy aplikacji sieci Web i nazwy skojarzonej grupy zasobów zostanie użyte odwołanie do obiektu.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="9cfd4-116">To odwołanie do obiektu jest tworzone przez pierwsze polecenie w przykładzie, w którym użyto polecenia **Get-AzureRmWebApp** w celu utworzenia odwołania do obiektu do aplikacji sieci Web o nazwie ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="9cfd4-117">Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="9cfd4-118">Ta zmienna i polecenie cmdlet **Get-AzureRmWebAppSSLBinding** są następnie używane przez drugie polecenie w celu uzyskania powiązań SSL.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="9cfd4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cfd4-119">PARAMETERS</span></span>

### <span data-ttu-id="9cfd4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cfd4-120">-DefaultProfile</span></span>
<span data-ttu-id="9cfd4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cfd4-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9cfd4-122">-Name</span></span>
<span data-ttu-id="9cfd4-123">Określa nazwę powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="9cfd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cfd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="9cfd4-125">Określa nazwę grupy zasobów, do której przypisano certyfikat.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="9cfd4-126">Nie można użyć parametru *ResourceGroupName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cfd4-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="9cfd4-127">-Slot</span></span>
<span data-ttu-id="9cfd4-128">Określa miejsce wdrożenia aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="9cfd4-129">Aby uzyskać miejsce do wdrożenia, użyj polecenia cmdlet Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cfd4-130">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="9cfd4-130">-WebApp</span></span>
<span data-ttu-id="9cfd4-131">Określa aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-131">Specifies a Web App.</span></span>
<span data-ttu-id="9cfd4-132">Aby uzyskać aplikację sieci Web, użyj polecenia cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cfd4-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="9cfd4-133">-WebAppName</span></span>
<span data-ttu-id="9cfd4-134">Określa nazwę aplikacji sieci Web, z której to polecenie cmdlet pobiera powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="9cfd4-135">Nie można użyć parametru *WebAppName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cfd4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfd4-136">CommonParameters</span></span>
<span data-ttu-id="9cfd4-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cfd4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfd4-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cfd4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfd4-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cfd4-139">INPUTS</span></span>

### <span data-ttu-id="9cfd4-140">Klienta</span><span class="sxs-lookup"><span data-stu-id="9cfd4-140">Site</span></span>
<span data-ttu-id="9cfd4-141">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="9cfd4-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9cfd4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cfd4-142">OUTPUTS</span></span>

## <span data-ttu-id="9cfd4-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cfd4-143">NOTES</span></span>

## <span data-ttu-id="9cfd4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cfd4-144">RELATED LINKS</span></span>

[<span data-ttu-id="9cfd4-145">Nowe — AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9cfd4-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="9cfd4-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9cfd4-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="9cfd4-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9cfd4-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


