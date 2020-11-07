---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: fda088ff8e8b3942ca6dbf94605b3887e3f6884b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888494"
---
# <span data-ttu-id="7c47b-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7c47b-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="7c47b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c47b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c47b-103">Usuwa powiązanie SSL z przekazanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="7c47b-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="7c47b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c47b-104">SYNTAX</span></span>

### <span data-ttu-id="7c47b-105">S1</span><span class="sxs-lookup"><span data-stu-id="7c47b-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c47b-106">S2</span><span class="sxs-lookup"><span data-stu-id="7c47b-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c47b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7c47b-107">DESCRIPTION</span></span>
<span data-ttu-id="7c47b-108">Polecenie cmdlet **Remove-AzWebAppSSLBinding** usuwa powiązanie SSL (Secure Sockets Layer) z aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7c47b-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="7c47b-109">Powiązania SSL są używane do kojarzenia aplikacji sieci Web z certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="7c47b-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="7c47b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c47b-110">EXAMPLES</span></span>

### <span data-ttu-id="7c47b-111">Przykład 1: Usuwanie powiązania SSL dla aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="7c47b-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="7c47b-112">To polecenie usuwa powiązanie SSL dla aplikacji sieci Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7c47b-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="7c47b-113">Ponieważ parametr *DeleteCertificate* nie jest uwzględniony, certyfikat zostanie usunięty, jeśli nie ma już żadnych powiązań SSL.</span><span class="sxs-lookup"><span data-stu-id="7c47b-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="7c47b-114">Przykład 2: Usuwanie powiązania SSL bez usuwania certyfikatu</span><span class="sxs-lookup"><span data-stu-id="7c47b-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="7c47b-115">Podobnie jak w przykładzie 1, to polecenie usuwa powiązanie SSL dla aplikacji sieci Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7c47b-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="7c47b-116">Jednak w tym przypadku jest uwzględniany parametr *DeleteCertificate* , a wartość parametru jest ustawiona na $false.</span><span class="sxs-lookup"><span data-stu-id="7c47b-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="7c47b-117">Oznacza to, że certyfikat nie zostanie usunięty bez względu na to, czy ma on jakiekolwiek powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="7c47b-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="7c47b-118">Przykład 3: Usuwanie powiązania SSL za pomocą odwołania do obiektu</span><span class="sxs-lookup"><span data-stu-id="7c47b-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="7c47b-119">W tym przykładzie użyto odwołania do obiektu w witrynie sieci Web aplikacji w celu usunięcia powiązania SSL dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7c47b-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="7c47b-120">W pierwszym poleceniu użyto polecenia cmdlet Get-AzWebApp w celu utworzenia odwołania do obiektu dla aplikacji sieci Web o nazwie ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7c47b-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="7c47b-121">Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.</span><span class="sxs-lookup"><span data-stu-id="7c47b-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="7c47b-122">Drugie polecenie używa odwołania do obiektu i polecenia cmdlet **Remove-AzWebAppSSLBinding** w celu usunięcia powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="7c47b-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="7c47b-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c47b-123">PARAMETERS</span></span>

### <span data-ttu-id="7c47b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c47b-124">-DefaultProfile</span></span>
<span data-ttu-id="7c47b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c47b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c47b-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="7c47b-126">-DeleteCertificate</span></span>
<span data-ttu-id="7c47b-127">Określa działanie, które ma zostać wykonane, jeśli usunięte powiązanie SSL jest jedynym powiązaniem używanym przez certyfikat.</span><span class="sxs-lookup"><span data-stu-id="7c47b-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="7c47b-128">Jeśli *DeleteCertificate* jest ustawiona na $false, certyfikat nie zostanie usunięty, gdy powiązanie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="7c47b-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="7c47b-129">Jeśli *DeleteCertificate* jest ustawiona na $true lub nie jest uwzględniona w poleceniu, certyfikat zostanie usunięty wraz z powiązaniem SSL.</span><span class="sxs-lookup"><span data-stu-id="7c47b-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="7c47b-130">Certyfikat zostanie usunięty tylko wtedy, gdy usunięte powiązanie SSL jest jedynym powiązaniem używanym przez certyfikat.</span><span class="sxs-lookup"><span data-stu-id="7c47b-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="7c47b-131">Jeśli certyfikat zawiera więcej niż jedno powiązanie, certyfikat nie zostanie usunięty bez względu na wartość parametru *DeleteCertificate* .</span><span class="sxs-lookup"><span data-stu-id="7c47b-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7c47b-132">-Force</span></span>
<span data-ttu-id="7c47b-133">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7c47b-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47b-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c47b-134">-Name</span></span>
<span data-ttu-id="7c47b-135">Określa nazwę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7c47b-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c47b-136">-ResourceGroupName</span></span>
<span data-ttu-id="7c47b-137">Określa nazwę grupy zasobów, do której przypisano certyfikat.</span><span class="sxs-lookup"><span data-stu-id="7c47b-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="7c47b-138">Nie można użyć parametru *ResourceGroupName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7c47b-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="7c47b-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="7c47b-139">-Slot</span></span>
<span data-ttu-id="7c47b-140">Określa miejsce wdrożenia aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7c47b-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="7c47b-141">Aby uzyskać miejsce do wdrożenia, użyj polecenia cmdlet Get-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="7c47b-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="7c47b-142">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7c47b-142">-WebApp</span></span>
<span data-ttu-id="7c47b-143">Określa aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7c47b-143">Specifies a Web App.</span></span>
<span data-ttu-id="7c47b-144">Aby uzyskać aplikację sieci Web, użyj polecenia cmdlet Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="7c47b-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="7c47b-145">Parametru *aplikacji* nie można używać w tym samym poleceniu, co parametr *ResourceGroupName* i/lub *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="7c47b-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="7c47b-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7c47b-146">-WebAppName</span></span>
<span data-ttu-id="7c47b-147">Określa nazwę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7c47b-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="7c47b-148">Nie można użyć parametru *WebAppName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7c47b-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="7c47b-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c47b-149">-Confirm</span></span>
<span data-ttu-id="7c47b-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c47b-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c47b-151">-WhatIf</span></span>
<span data-ttu-id="7c47b-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c47b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c47b-153">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c47b-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c47b-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c47b-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c47b-155">CommonParameters</span></span>
<span data-ttu-id="7c47b-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c47b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c47b-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c47b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c47b-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c47b-158">INPUTS</span></span>

### <span data-ttu-id="7c47b-159">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="7c47b-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7c47b-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c47b-160">OUTPUTS</span></span>

### <span data-ttu-id="7c47b-161">System. void</span><span class="sxs-lookup"><span data-stu-id="7c47b-161">System.Void</span></span>

## <span data-ttu-id="7c47b-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c47b-162">NOTES</span></span>

## <span data-ttu-id="7c47b-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c47b-163">RELATED LINKS</span></span>

[<span data-ttu-id="7c47b-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7c47b-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="7c47b-165">Nowe — AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7c47b-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="7c47b-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c47b-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="7c47b-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c47b-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


