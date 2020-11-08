---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054496"
---
# <span data-ttu-id="a91fa-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a91fa-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="a91fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a91fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a91fa-103">Pobiera ustawienia agenta IaaS programu SQL Server na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a91fa-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="a91fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a91fa-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a91fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a91fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a91fa-106">Polecenie cmdlet **Get-AzureVMSqlServerExtension** pobiera ustawienia infrastruktury programu SQL Server jako agenta usługi (IaaS) na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a91fa-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="a91fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a91fa-107">EXAMPLES</span></span>

### <span data-ttu-id="a91fa-108">Przykład 1: uzyskiwanie ustawień rozszerzenia serwera SQL na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a91fa-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="a91fa-109">Pobiera ustawienia rozszerzenia programu SQL Server na konkretnej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a91fa-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="a91fa-110">Przykład 2: uzyskiwanie ustawień agenta usługi SQL Server IaaS Agent na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a91fa-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="a91fa-111">Pobiera ustawienia agenta IaaS programu SQL Server na konkretnej maszynie wirtualnej za pomocą wejścia potokowego.</span><span class="sxs-lookup"><span data-stu-id="a91fa-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="a91fa-112">Przykład 3: uzyskiwanie ustawień konkretnego agenta programu SQL Server w wersji IaaS na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a91fa-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="a91fa-113">To polecenie pobiera ustawienia konkretnej wersji agenta usługi SQL Server IaaS na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a91fa-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="a91fa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a91fa-114">PARAMETERS</span></span>

### <span data-ttu-id="a91fa-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a91fa-115">-InformationAction</span></span>
<span data-ttu-id="a91fa-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="a91fa-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a91fa-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a91fa-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a91fa-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="a91fa-118">Continue</span></span>
- <span data-ttu-id="a91fa-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="a91fa-119">Ignore</span></span>
- <span data-ttu-id="a91fa-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="a91fa-120">Inquire</span></span>
- <span data-ttu-id="a91fa-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a91fa-121">SilentlyContinue</span></span>
- <span data-ttu-id="a91fa-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="a91fa-122">Stop</span></span>
- <span data-ttu-id="a91fa-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="a91fa-123">Suspend</span></span>

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

### <span data-ttu-id="a91fa-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a91fa-124">-InformationVariable</span></span>
<span data-ttu-id="a91fa-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="a91fa-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a91fa-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="a91fa-126">-Profile</span></span>
<span data-ttu-id="a91fa-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a91fa-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a91fa-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a91fa-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a91fa-129">-VM</span><span class="sxs-lookup"><span data-stu-id="a91fa-129">-VM</span></span>
<span data-ttu-id="a91fa-130">Określa obiekt trwałej maszyny wirtualnej, z którego będą pobierane ustawienia tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a91fa-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a91fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91fa-131">CommonParameters</span></span>
<span data-ttu-id="a91fa-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a91fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91fa-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91fa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91fa-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a91fa-134">INPUTS</span></span>

## <span data-ttu-id="a91fa-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a91fa-135">OUTPUTS</span></span>

## <span data-ttu-id="a91fa-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a91fa-136">NOTES</span></span>

## <span data-ttu-id="a91fa-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a91fa-137">RELATED LINKS</span></span>

[<span data-ttu-id="a91fa-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a91fa-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="a91fa-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a91fa-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


