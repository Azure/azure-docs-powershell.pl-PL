---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 3e3fea3e43f2370347ae819604d6caf1e830ebd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548436"
---
# <span data-ttu-id="82120-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="82120-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="82120-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82120-102">SYNOPSIS</span></span>
<span data-ttu-id="82120-103">Ustawia niestandardową konfigurację nazwy hosta dla serwera proxy lub portalu usługi zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="82120-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82120-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82120-104">SYNTAX</span></span>

### <span data-ttu-id="82120-105">Określona usługa zarządzania interfejsem API (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="82120-105">Specific API Management service (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82120-106">Ustaw z udostępnionego wystąpienia PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="82120-106">Set from provided PsApiManagement instance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82120-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82120-107">DESCRIPTION</span></span>
<span data-ttu-id="82120-108">Polecenie cmdlet **Set-AzureRmApiManagementHostnames** powoduje zastosowanie niestandardowej konfiguracji nazwy hosta dla serwera proxy lub portalu usługi zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="82120-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="82120-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82120-109">EXAMPLES</span></span>

### <span data-ttu-id="82120-110">Przykład 1: Ustawianie niestandardowej konfiguracji hostów dla serwera proxy i portalu</span><span class="sxs-lookup"><span data-stu-id="82120-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="82120-111">To polecenie ustawia niestandardową konfigurację nazwy hosta dla serwera proxy i portalu.</span><span class="sxs-lookup"><span data-stu-id="82120-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="82120-112">Przykład 2: Konfigurowanie niestandardowej nazwy hosta dla serwera proxy i portalu</span><span class="sxs-lookup"><span data-stu-id="82120-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="82120-113">W tym przykładzie konfigurujesz niestandardową nazwę hosta dla serwera proxy i portalu.</span><span class="sxs-lookup"><span data-stu-id="82120-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="82120-114">Musisz zaimportować odpowiednie certyfikaty, a następnie zastosować niestandardowe nazwy hostów.</span><span class="sxs-lookup"><span data-stu-id="82120-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="82120-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82120-115">PARAMETERS</span></span>

### <span data-ttu-id="82120-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82120-116">-ApiManagement</span></span>
<span data-ttu-id="82120-117">Określa wystąpienie **PsApiManagement** , z którego to polecenie cmdlet pobiera parametry *PortalHostnameConfiguration* i *ProxyHostnameConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="82120-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Set from provided PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82120-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82120-118">-Name</span></span>
<span data-ttu-id="82120-119">Określa nazwę wystąpienia zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="82120-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82120-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82120-120">-PassThru</span></span>
<span data-ttu-id="82120-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="82120-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82120-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="82120-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82120-123">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="82120-123">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="82120-124">Określa konfigurację niestandardowej nazwy hosta portalu.</span><span class="sxs-lookup"><span data-stu-id="82120-124">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="82120-125">Przekazanie $null do polecenia cmdlet powoduje ustawienie domyślnej nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="82120-125">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82120-126">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="82120-126">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="82120-127">Określa konfigurację niestandardowej nazwy hosta proxy.</span><span class="sxs-lookup"><span data-stu-id="82120-127">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="82120-128">Przekazywanie $null ustawia domyślną nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="82120-128">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82120-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82120-129">-ResourceGroupName</span></span>
<span data-ttu-id="82120-130">Określa nazwę grupy zasobów, w której istnieje wystąpienie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="82120-130">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82120-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82120-131">-DefaultProfile</span></span>
<span data-ttu-id="82120-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82120-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82120-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82120-133">CommonParameters</span></span>
<span data-ttu-id="82120-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82120-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82120-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82120-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82120-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82120-136">INPUTS</span></span>

### <span data-ttu-id="82120-137">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="82120-137">PsApiManagement</span></span>
<span data-ttu-id="82120-138">Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="82120-138">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="82120-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82120-139">OUTPUTS</span></span>

### <span data-ttu-id="82120-140">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="82120-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="82120-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82120-141">NOTES</span></span>

## <span data-ttu-id="82120-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82120-142">RELATED LINKS</span></span>

[<span data-ttu-id="82120-143">Import — AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="82120-143">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="82120-144">Nowe — AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="82120-144">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


