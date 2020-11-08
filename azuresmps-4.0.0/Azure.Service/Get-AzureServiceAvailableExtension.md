---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054572"
---
# <span data-ttu-id="09ebf-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="09ebf-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="09ebf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="09ebf-103">Pobiera informacje na temat dostępnych rozszerzeń usług hostowanych.</span><span class="sxs-lookup"><span data-stu-id="09ebf-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="09ebf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09ebf-104">SYNTAX</span></span>

### <span data-ttu-id="09ebf-105">ListLatestExtensions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="09ebf-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="09ebf-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="09ebf-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="09ebf-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="09ebf-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="09ebf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="09ebf-108">DESCRIPTION</span></span>
<span data-ttu-id="09ebf-109">Polecenie cmdlet **Get-AzureServiceAvailableExtension** pobiera informacje dotyczące najnowszych dostępnych rozszerzeń usług hostowanych.</span><span class="sxs-lookup"><span data-stu-id="09ebf-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="09ebf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09ebf-110">EXAMPLES</span></span>

### <span data-ttu-id="09ebf-111">Przykład 1: Uzyskaj dostępne rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="09ebf-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="09ebf-112">To polecenie pobiera wszystkie dostępne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="09ebf-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="09ebf-113">Przykład 2: uzyskiwanie rozszerzeń w określonym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="09ebf-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="09ebf-114">To polecenie pobiera rozszerzenia o określonej nazwie w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="09ebf-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="09ebf-115">Przykład 3: uzyskiwanie określonej wersji rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="09ebf-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="09ebf-116">To polecenie pobiera informacje o konkretnej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="09ebf-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="09ebf-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09ebf-117">PARAMETERS</span></span>

### <span data-ttu-id="09ebf-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="09ebf-118">-AllVersions</span></span>
<span data-ttu-id="09ebf-119">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="09ebf-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebf-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="09ebf-120">-ExtensionName</span></span>
<span data-ttu-id="09ebf-121">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="09ebf-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebf-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="09ebf-122">-InformationAction</span></span>
<span data-ttu-id="09ebf-123">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="09ebf-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="09ebf-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="09ebf-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09ebf-125">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="09ebf-125">Continue</span></span>
- <span data-ttu-id="09ebf-126">Ignorować</span><span class="sxs-lookup"><span data-stu-id="09ebf-126">Ignore</span></span>
- <span data-ttu-id="09ebf-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="09ebf-127">Inquire</span></span>
- <span data-ttu-id="09ebf-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="09ebf-128">SilentlyContinue</span></span>
- <span data-ttu-id="09ebf-129">Przestaw</span><span class="sxs-lookup"><span data-stu-id="09ebf-129">Stop</span></span>
- <span data-ttu-id="09ebf-130">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="09ebf-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ebf-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09ebf-131">-InformationVariable</span></span>
<span data-ttu-id="09ebf-132">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="09ebf-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ebf-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="09ebf-133">-Profile</span></span>
<span data-ttu-id="09ebf-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09ebf-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="09ebf-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="09ebf-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ebf-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="09ebf-136">-ProviderNamespace</span></span>
<span data-ttu-id="09ebf-137">Określa obszar nazw dostawcy rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="09ebf-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebf-138">-Version</span><span class="sxs-lookup"><span data-stu-id="09ebf-138">-Version</span></span>
<span data-ttu-id="09ebf-139">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="09ebf-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ebf-140">CommonParameters</span></span>
<span data-ttu-id="09ebf-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ebf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ebf-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ebf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ebf-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09ebf-143">INPUTS</span></span>

## <span data-ttu-id="09ebf-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09ebf-144">OUTPUTS</span></span>

## <span data-ttu-id="09ebf-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09ebf-145">NOTES</span></span>

## <span data-ttu-id="09ebf-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09ebf-146">RELATED LINKS</span></span>

[<span data-ttu-id="09ebf-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="09ebf-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


