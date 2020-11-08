---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055510"
---
# <span data-ttu-id="de6fd-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="de6fd-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="de6fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="de6fd-103">Pobiera informacje dotyczące najnowszych dostępnych rozszerzeń dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="de6fd-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="de6fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de6fd-104">SYNTAX</span></span>

### <span data-ttu-id="de6fd-105">ListLatestExtensions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de6fd-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="de6fd-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="de6fd-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="de6fd-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="de6fd-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="de6fd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="de6fd-108">DESCRIPTION</span></span>
<span data-ttu-id="de6fd-109">Polecenie cmdlet **Get-AzureVMAvailableExtension** pobiera informacje dotyczące najnowszych dostępnych rozszerzeń dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="de6fd-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="de6fd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de6fd-110">EXAMPLES</span></span>

### <span data-ttu-id="de6fd-111">Przykład 1: uzyskiwanie informacji na temat najnowszych dostępnych rozszerzeń</span><span class="sxs-lookup"><span data-stu-id="de6fd-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="de6fd-112">To polecenie pobiera informacje dotyczące najnowszych dostępnych rozszerzeń dla wszystkich maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="de6fd-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="de6fd-113">Przykład 2: uzyskiwanie informacji z określonej nazwy rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="de6fd-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="de6fd-114">To polecenie pobiera informacje ze wszystkich wersji rozszerzenia o nazwie VMAccessAgent oraz wydawcy o nazwie Microsoft. Computer.</span><span class="sxs-lookup"><span data-stu-id="de6fd-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="de6fd-115">Przykład 3: uzyskiwanie informacji z określonego rozszerzenia maszyny wirtualnej według numeru wersji</span><span class="sxs-lookup"><span data-stu-id="de6fd-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="de6fd-116">To polecenie pobiera informacje o rozszerzeniu o nazwie VMAccessAgent oraz wydawcy o nazwie Microsoft. COMPUTE dla rozszerzenia wersja 1.0.3.</span><span class="sxs-lookup"><span data-stu-id="de6fd-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="de6fd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de6fd-117">PARAMETERS</span></span>

### <span data-ttu-id="de6fd-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="de6fd-118">-AllVersions</span></span>
<span data-ttu-id="de6fd-119">Wskazuje, że w tym poleceniu cmdlet są wyświetlane wszystkie wersje rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="de6fd-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="de6fd-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="de6fd-120">-ExtensionName</span></span>
<span data-ttu-id="de6fd-121">Określa nazwę dostępnego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="de6fd-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="de6fd-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="de6fd-122">-InformationAction</span></span>
<span data-ttu-id="de6fd-123">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="de6fd-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="de6fd-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="de6fd-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de6fd-125">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="de6fd-125">Continue</span></span>
- <span data-ttu-id="de6fd-126">Ignorować</span><span class="sxs-lookup"><span data-stu-id="de6fd-126">Ignore</span></span>
- <span data-ttu-id="de6fd-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="de6fd-127">Inquire</span></span>
- <span data-ttu-id="de6fd-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="de6fd-128">SilentlyContinue</span></span>
- <span data-ttu-id="de6fd-129">Przestaw</span><span class="sxs-lookup"><span data-stu-id="de6fd-129">Stop</span></span>
- <span data-ttu-id="de6fd-130">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="de6fd-130">Suspend</span></span>

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

### <span data-ttu-id="de6fd-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="de6fd-131">-InformationVariable</span></span>
<span data-ttu-id="de6fd-132">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="de6fd-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="de6fd-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="de6fd-133">-Profile</span></span>
<span data-ttu-id="de6fd-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de6fd-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de6fd-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="de6fd-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de6fd-136">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="de6fd-136">-Publisher</span></span>
<span data-ttu-id="de6fd-137">Określa wydawcę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="de6fd-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="de6fd-138">-Version</span><span class="sxs-lookup"><span data-stu-id="de6fd-138">-Version</span></span>
<span data-ttu-id="de6fd-139">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="de6fd-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="de6fd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6fd-140">CommonParameters</span></span>
<span data-ttu-id="de6fd-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de6fd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6fd-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de6fd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6fd-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de6fd-143">INPUTS</span></span>

## <span data-ttu-id="de6fd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de6fd-144">OUTPUTS</span></span>

## <span data-ttu-id="de6fd-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de6fd-145">NOTES</span></span>

## <span data-ttu-id="de6fd-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de6fd-146">RELATED LINKS</span></span>

