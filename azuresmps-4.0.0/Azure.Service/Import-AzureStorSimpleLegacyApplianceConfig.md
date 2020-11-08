---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055225"
---
# <span data-ttu-id="3b313-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="3b313-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="3b313-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b313-102">SYNOPSIS</span></span>
<span data-ttu-id="3b313-103">Importuje plik konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3b313-103">Imports a configuration file.</span></span>

## <span data-ttu-id="3b313-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b313-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b313-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b313-105">DESCRIPTION</span></span>
<span data-ttu-id="3b313-106">Polecenie cmdlet **Import-AzureStorSimpleLegacyApplianceConfig** importuje plik konfiguracji ze starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3b313-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="3b313-107">Ten plik zawiera informacje na temat kontenerów woluminów, zasad tworzenia kopii zapasowych i poświadczeń konta magazynu dla usługi Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="3b313-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="3b313-108">To polecenie cmdlet zwraca metadane konfiguracji starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3b313-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="3b313-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b313-109">EXAMPLES</span></span>

### <span data-ttu-id="3b313-110">Przykład 1: Importowanie pliku konfiguracji</span><span class="sxs-lookup"><span data-stu-id="3b313-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="3b313-111">To polecenie umożliwia zaimportowanie pliku konfiguracji w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="3b313-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="3b313-112">Polecenie zawiera klucz do odszyfrowania pliku.</span><span class="sxs-lookup"><span data-stu-id="3b313-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="3b313-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b313-113">PARAMETERS</span></span>

### <span data-ttu-id="3b313-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="3b313-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="3b313-115">Określa klucz odszyfrowywania konfiguracji starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3b313-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="3b313-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="3b313-116">-ConfigFilePath</span></span>
<span data-ttu-id="3b313-117">Określa absolutną ścieżkę pliku konfiguracji, który należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="3b313-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b313-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="3b313-118">-Profile</span></span>
<span data-ttu-id="3b313-119">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3b313-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3b313-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="3b313-120">-TargetDeviceName</span></span>
<span data-ttu-id="3b313-121">Określa nazwę urządzenia docelowego, która jest wyświetlana w portalu.</span><span class="sxs-lookup"><span data-stu-id="3b313-121">Specifies the name of the target device as presented in the portal.</span></span>

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

### <span data-ttu-id="3b313-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b313-122">CommonParameters</span></span>
<span data-ttu-id="3b313-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b313-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b313-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b313-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b313-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b313-125">INPUTS</span></span>

### <span data-ttu-id="3b313-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3b313-126">None</span></span>

## <span data-ttu-id="3b313-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b313-127">OUTPUTS</span></span>

### <span data-ttu-id="3b313-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b313-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="3b313-129">To polecenie cmdlet zwraca szczegóły konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3b313-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="3b313-130">Obiekt **LegacyApplianceConfiguration** zawiera następujące informacje: Identyfikator konfiguracji, nazwy kontenerów woluminów, rekordy kontroli dostępu, zasady tworzenia kopii zapasowych, ustawienia przepustowości, kontenery woluminów, poświadczenia konta magazynu i woluminy.</span><span class="sxs-lookup"><span data-stu-id="3b313-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="3b313-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b313-131">NOTES</span></span>

## <span data-ttu-id="3b313-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b313-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b313-133">Import — AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3b313-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


