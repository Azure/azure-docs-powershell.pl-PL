---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 9c5f819a34ea0e394888e8156dad7a897d18167f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553059"
---
# <span data-ttu-id="3e41c-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3e41c-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="3e41c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e41c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e41c-103">Importuje certyfikat w formacie PFX dla usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3e41c-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e41c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e41c-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e41c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e41c-105">DESCRIPTION</span></span>
<span data-ttu-id="3e41c-106">Polecenie cmdlet **Import-AzureRmApiManagementHostnameCertificate** importuje certyfikat w formacie PFX dla usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3e41c-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="3e41c-107">Certyfikat ma być stosowany do konfiguracji niestandardowych nazw hostów.</span><span class="sxs-lookup"><span data-stu-id="3e41c-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="3e41c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e41c-108">EXAMPLES</span></span>

### <span data-ttu-id="3e41c-109">Przykład 1: Importowanie certyfikatu hosta zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="3e41c-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="3e41c-110">To polecenie importuje certyfikat dla niestandardowej nazwy hosta serwera proxy.</span><span class="sxs-lookup"><span data-stu-id="3e41c-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="3e41c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e41c-111">PARAMETERS</span></span>

### <span data-ttu-id="3e41c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e41c-112">-DefaultProfile</span></span>
<span data-ttu-id="3e41c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e41c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3e41c-114">-Nazwa_hostatype</span><span class="sxs-lookup"><span data-stu-id="3e41c-114">-HostnameType</span></span>
<span data-ttu-id="3e41c-115">Określa typ nazwy hosta, dla którego to polecenie cmdlet ładuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="3e41c-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="3e41c-116">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3e41c-116">Valid values are:</span></span> 

- <span data-ttu-id="3e41c-117">Serwerem</span><span class="sxs-lookup"><span data-stu-id="3e41c-117">Proxy</span></span>
- <span data-ttu-id="3e41c-118">Portalu</span><span class="sxs-lookup"><span data-stu-id="3e41c-118">Portal</span></span>

```yaml
Type: PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e41c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e41c-119">-Name</span></span>
<span data-ttu-id="3e41c-120">Określa nazwę wdrożenia zarządzania interfejsem API, które zostało zaimportowane za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e41c-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e41c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e41c-121">-PassThru</span></span>
<span data-ttu-id="3e41c-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3e41c-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e41c-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3e41c-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e41c-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="3e41c-124">-PfxPassword</span></span>
<span data-ttu-id="3e41c-125">Określa hasło do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="3e41c-125">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e41c-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="3e41c-126">-PfxPath</span></span>
<span data-ttu-id="3e41c-127">Określa ścieżkę do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="3e41c-127">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e41c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e41c-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e41c-129">Określa nazwę grupy zasobów, w której istnieje wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3e41c-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e41c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e41c-130">CommonParameters</span></span>
<span data-ttu-id="3e41c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e41c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e41c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e41c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e41c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e41c-133">INPUTS</span></span>

### <span data-ttu-id="3e41c-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3e41c-134">None</span></span>
<span data-ttu-id="3e41c-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3e41c-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e41c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e41c-136">OUTPUTS</span></span>

### <span data-ttu-id="3e41c-137">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3e41c-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="3e41c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e41c-138">NOTES</span></span>

## <span data-ttu-id="3e41c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e41c-139">RELATED LINKS</span></span>

[<span data-ttu-id="3e41c-140">Nowe — AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e41c-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="3e41c-141">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3e41c-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


