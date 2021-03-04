---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: b1d9aa1f212ce31a8bb7fadeff4e0ca8afcf05e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959313"
---
# <span data-ttu-id="af130-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="af130-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="af130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af130-102">SYNOPSIS</span></span>
<span data-ttu-id="af130-103">Usuwa powiązanie SSL z przekazanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="af130-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="af130-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="af130-104">SYNTAX</span></span>

### <span data-ttu-id="af130-105">S1</span><span class="sxs-lookup"><span data-stu-id="af130-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af130-106">S2</span><span class="sxs-lookup"><span data-stu-id="af130-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af130-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="af130-107">DESCRIPTION</span></span>
<span data-ttu-id="af130-108">Polecenie **cmdlet Remove-AzWebAppSSLBinding** usuwa powiązanie Secure Sockets Layer (SSL) z aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="af130-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="af130-109">Powiązania SSL służą do kojarzenia aplikacji sieci Web z certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="af130-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="af130-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="af130-110">EXAMPLES</span></span>

### <span data-ttu-id="af130-111">Przykład 1. Usuwanie powiązania SSL dla aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="af130-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="af130-112">To polecenie usuwa powiązanie SSL dla aplikacji sieci Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="af130-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="af130-113">Ponieważ parametr *DeleteCertificate* nie jest uwzględniany, certyfikat zostanie usunięty, jeśli nie ma już żadnych powiązań SSL.</span><span class="sxs-lookup"><span data-stu-id="af130-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="af130-114">Przykład 2. Usuwanie powiązania SSL bez usuwania certyfikatu</span><span class="sxs-lookup"><span data-stu-id="af130-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="af130-115">Podobnie jak w przykładzie 1, to polecenie usuwa również powiązanie SSL dla aplikacji Sieci Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="af130-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="af130-116">Jednak w tym przypadku parametr *DeleteCertificate* jest uwzględniany, a wartość parametru jest ustawiana jako $False.</span><span class="sxs-lookup"><span data-stu-id="af130-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="af130-117">Oznacza to, że certyfikat nie zostanie usunięty bez względu na to, czy ma jakiekolwiek powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="af130-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="af130-118">Przykład 3. Usuwanie powiązania SSL za pomocą odwołania do obiektu</span><span class="sxs-lookup"><span data-stu-id="af130-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="af130-119">W tym przykładzie do usunięcia powiązania SSL dla aplikacji sieci Web jest używane odwołanie do obiektu witryny internetowej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af130-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="af130-120">Pierwsze polecenie używa Get-AzWebApp cmdlet w celu utworzenia odwołania do obiektu aplikacji Sieci Web o nazwie ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="af130-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="af130-121">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $WebApp.</span><span class="sxs-lookup"><span data-stu-id="af130-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="af130-122">Drugie polecenie używa odwołania do obiektu i polecenia **cmdlet Remove-AzWebAppSSLBinding** w celu usunięcia powiązania SSL.</span><span class="sxs-lookup"><span data-stu-id="af130-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="af130-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af130-123">PARAMETERS</span></span>

### <span data-ttu-id="af130-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af130-124">-DefaultProfile</span></span>
<span data-ttu-id="af130-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="af130-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af130-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="af130-126">-DeleteCertificate</span></span>
<span data-ttu-id="af130-127">Określa akcję do podjęcia w przypadku usunięcia powiązania SSL jest jedynym powiązaniem używanym w certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="af130-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="af130-128">Jeśli *wartość DeleteCertificate* $False, certyfikat nie zostanie usunięty po usunięciu powiązania.</span><span class="sxs-lookup"><span data-stu-id="af130-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="af130-129">Jeśli *wartość DeleteCertificate* $True lub nie jest zawarta w poleceniu, certyfikat zostanie usunięty wraz z powiązaniem SSL.</span><span class="sxs-lookup"><span data-stu-id="af130-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="af130-130">Certyfikat zostanie usunięty tylko w przypadku usunięcia powiązania SSL jest jedynym używanym w certyfikacie powiązaniem.</span><span class="sxs-lookup"><span data-stu-id="af130-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="af130-131">Jeśli certyfikat ma więcej niż jedno powiązanie, certyfikat nie zostanie usunięty niezależnie od wartości parametru *DeleteCertificate.*</span><span class="sxs-lookup"><span data-stu-id="af130-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

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

### <span data-ttu-id="af130-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="af130-132">-Force</span></span>
<span data-ttu-id="af130-133">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="af130-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af130-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="af130-134">-Name</span></span>
<span data-ttu-id="af130-135">Określa nazwę aplikacji Sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af130-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="af130-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af130-136">-ResourceGroupName</span></span>
<span data-ttu-id="af130-137">Określa nazwę grupy zasobów, do których jest przypisany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="af130-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="af130-138">W tym samym *poleceniu nie można* użyć parametru ResourceGroupName ani *parametru WebApp.*</span><span class="sxs-lookup"><span data-stu-id="af130-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="af130-139">— Slot</span><span class="sxs-lookup"><span data-stu-id="af130-139">-Slot</span></span>
<span data-ttu-id="af130-140">Określa miejsce wdrożenia aplikacji Sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af130-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="af130-141">Aby uzyskać miejsce wdrożenia, użyj Get-AzWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af130-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="af130-142">- WebApp</span><span class="sxs-lookup"><span data-stu-id="af130-142">-WebApp</span></span>
<span data-ttu-id="af130-143">Określa aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af130-143">Specifies a Web App.</span></span>
<span data-ttu-id="af130-144">Aby uzyskać aplikację Sieci Web, użyj Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af130-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="af130-145">Nie można użyć *parametru WebApp* w tym samym poleceniu co parametr *ResourceGroupName* i/lub *nazwa_sieci Web.*</span><span class="sxs-lookup"><span data-stu-id="af130-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="af130-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="af130-146">-WebAppName</span></span>
<span data-ttu-id="af130-147">Określa nazwę aplikacji Sieci Web.</span><span class="sxs-lookup"><span data-stu-id="af130-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="af130-148">W tym samym poleceniu nie można użyć parametru *WebAppName* ani parametru *WebApp.*</span><span class="sxs-lookup"><span data-stu-id="af130-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="af130-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af130-149">-Confirm</span></span>
<span data-ttu-id="af130-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="af130-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af130-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af130-151">-WhatIf</span></span>
<span data-ttu-id="af130-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af130-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af130-153">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af130-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af130-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="af130-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af130-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af130-155">CommonParameters</span></span>
<span data-ttu-id="af130-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af130-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af130-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af130-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af130-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af130-158">INPUTS</span></span>

### <span data-ttu-id="af130-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="af130-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="af130-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af130-160">OUTPUTS</span></span>

### <span data-ttu-id="af130-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="af130-161">System.Void</span></span>

## <span data-ttu-id="af130-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="af130-162">NOTES</span></span>

## <span data-ttu-id="af130-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af130-163">RELATED LINKS</span></span>

[<span data-ttu-id="af130-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="af130-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="af130-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="af130-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="af130-166">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="af130-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="af130-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="af130-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


