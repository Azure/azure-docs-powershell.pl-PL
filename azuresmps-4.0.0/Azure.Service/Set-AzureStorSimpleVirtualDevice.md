---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054401"
---
# <span data-ttu-id="a925e-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="a925e-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="a925e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a925e-102">SYNOPSIS</span></span>
<span data-ttu-id="a925e-103">Umożliwia utworzenie lub zaktualizowanie konfiguracji urządzenia wirtualnego StorSimple.</span><span class="sxs-lookup"><span data-stu-id="a925e-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="a925e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a925e-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a925e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a925e-105">DESCRIPTION</span></span>
<span data-ttu-id="a925e-106">Polecenie cmdlet **Set-AzureStorSimpleVirtualDevice** umożliwia utworzenie lub zaktualizowanie konfiguracji urządzenia wirtualnego Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="a925e-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="a925e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a925e-107">EXAMPLES</span></span>

### <span data-ttu-id="a925e-108">Przykład 1: Aktualizowanie urządzenia wirtualnego</span><span class="sxs-lookup"><span data-stu-id="a925e-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="a925e-109">W pierwszym poleceniu użyto klasy **System. TimeZoneInfo** .NET i składni standardowej, aby uzyskać standardową strefę czasową w Pacyfiku i przechowywać ten obiekt w zmiennej $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="a925e-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="a925e-110">Drugie polecenie zaktualizuje urządzenie o nazwie Contoso23, aby korzystała z strefy czasowej określonej w $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="a925e-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="a925e-111">Polecenie wymaga klucza tajnego w celu uzyskania dostępu do konfiguracji urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a925e-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="a925e-112">Przykład 2: Aktualizowanie urządzenia wirtualnego przy użyciu operatora potoku</span><span class="sxs-lookup"><span data-stu-id="a925e-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="a925e-113">To polecenie powoduje zaktualizowanie urządzenia o nazwie Contoso23 w celu użycia strefy czasowej tworzonego przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="a925e-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="a925e-114">Polecenie wymaga klucza tajnego w celu uzyskania dostępu do konfiguracji urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a925e-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="a925e-115">To polecenie działa w ten sam sposób, co w poprzednim przykładzie, ale przekazuje strefę czasową do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a925e-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="a925e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a925e-116">PARAMETERS</span></span>

### <span data-ttu-id="a925e-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="a925e-117">-AdministratorPassword</span></span>
<span data-ttu-id="a925e-118">Określa hasło administratora urządzenia wirtualnego do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="a925e-118">Specifies the administrator password of the virtual device to configure.</span></span>

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

### <span data-ttu-id="a925e-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a925e-119">-DeviceName</span></span>
<span data-ttu-id="a925e-120">Określa nazwę urządzenia wirtualnego do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="a925e-120">Specifies the name of the virtual device to configure.</span></span>

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

### <span data-ttu-id="a925e-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="a925e-121">-Profile</span></span>
<span data-ttu-id="a925e-122">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a925e-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a925e-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="a925e-123">-SecretKey</span></span>
<span data-ttu-id="a925e-124">Określa klucz szyfrowania usługi dla urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a925e-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="a925e-125">Ten klucz jest generowany po zarejestrowaniu pierwszego urządzenia fizycznego za pomocą zasobu.</span><span class="sxs-lookup"><span data-stu-id="a925e-125">This key is generated when the first physical device is registered with a resource.</span></span>

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

### <span data-ttu-id="a925e-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="a925e-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="a925e-127">Określa hasło Menedżera migawek.</span><span class="sxs-lookup"><span data-stu-id="a925e-127">Specifies the snapshot manager password.</span></span>

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

### <span data-ttu-id="a925e-128">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="a925e-128">-TimeZone</span></span>
<span data-ttu-id="a925e-129">Określa strefę czasową dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a925e-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="a925e-130">Obiekt **TimeZoneInfo** można utworzyć przy użyciu metody **GetSystemTimeZone ()** .</span><span class="sxs-lookup"><span data-stu-id="a925e-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="a925e-131">Na przykład to polecenie tworzy obiekt informacji o strefie czasowej dla Pacyficznyego czasu standardowego: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="a925e-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a925e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a925e-132">CommonParameters</span></span>
<span data-ttu-id="a925e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a925e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a925e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a925e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a925e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a925e-135">INPUTS</span></span>

### <span data-ttu-id="a925e-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="a925e-136">TimeZoneInfo</span></span>
<span data-ttu-id="a925e-137">Do tego polecenia cmdlet można nawiązać obiekt **TimeZoneInfo** .</span><span class="sxs-lookup"><span data-stu-id="a925e-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="a925e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a925e-138">OUTPUTS</span></span>

### <span data-ttu-id="a925e-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="a925e-139">DeviceJobDetails</span></span>
<span data-ttu-id="a925e-140">To polecenie cmdlet zwraca zaktualizowane dane urządzenia dla urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a925e-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="a925e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a925e-141">NOTES</span></span>

## <span data-ttu-id="a925e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a925e-142">RELATED LINKS</span></span>

[<span data-ttu-id="a925e-143">Nowe — AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="a925e-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="a925e-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="a925e-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


