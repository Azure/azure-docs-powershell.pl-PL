---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 490f7b4a0cb723d02deb1d18e8a2ddfb993e7f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050643"
---
# <span data-ttu-id="616cd-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="616cd-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="616cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="616cd-102">SYNOPSIS</span></span>

## <span data-ttu-id="616cd-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="616cd-103">SYNTAX</span></span>

### <span data-ttu-id="616cd-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="616cd-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="616cd-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="616cd-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="616cd-106">Opis</span><span class="sxs-lookup"><span data-stu-id="616cd-106">DESCRIPTION</span></span>
<span data-ttu-id="616cd-107">Polecenie cmdlet **Edit-AzWebAppBackupConfiguration** umożliwia edytowanie bieżącej kopii zapasowej konfiguracji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="616cd-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="616cd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="616cd-108">EXAMPLES</span></span>

## <span data-ttu-id="616cd-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="616cd-109">PARAMETERS</span></span>

### <span data-ttu-id="616cd-110">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="616cd-110">-Databases</span></span>
<span data-ttu-id="616cd-111">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="616cd-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="616cd-112">-DefaultProfile</span></span>
<span data-ttu-id="616cd-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="616cd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="616cd-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="616cd-114">-FrequencyInterval</span></span>
<span data-ttu-id="616cd-115">Interwał częstotliwości</span><span class="sxs-lookup"><span data-stu-id="616cd-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="616cd-116">-FrequencyUnit</span></span>
<span data-ttu-id="616cd-117">Jednostka częstotliwości</span><span class="sxs-lookup"><span data-stu-id="616cd-117">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="616cd-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="616cd-119">Zachowywanie co najmniej jednej opcji kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="616cd-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="616cd-120">-Name</span></span>
<span data-ttu-id="616cd-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="616cd-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="616cd-122">-ResourceGroupName</span></span>
<span data-ttu-id="616cd-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="616cd-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="616cd-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="616cd-125">Okres przechowywania w dniach</span><span class="sxs-lookup"><span data-stu-id="616cd-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="616cd-126">-Slot</span></span>
<span data-ttu-id="616cd-127">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="616cd-127">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="616cd-128">-StartTime</span></span>
<span data-ttu-id="616cd-129">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="616cd-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="616cd-130">-StorageAccountUrl</span></span>
<span data-ttu-id="616cd-131">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="616cd-131">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-132">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="616cd-132">-WebApp</span></span>
<span data-ttu-id="616cd-133">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="616cd-133">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616cd-134">CommonParameters</span></span>
<span data-ttu-id="616cd-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616cd-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="616cd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616cd-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="616cd-137">INPUTS</span></span>

### <span data-ttu-id="616cd-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="616cd-138">System.Int32</span></span>

### <span data-ttu-id="616cd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="616cd-139">System.String</span></span>

### <span data-ttu-id="616cd-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="616cd-140">System.DateTime</span></span>

### <span data-ttu-id="616cd-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="616cd-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="616cd-142">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="616cd-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="616cd-143">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="616cd-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="616cd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="616cd-144">OUTPUTS</span></span>

### <span data-ttu-id="616cd-145">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="616cd-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="616cd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="616cd-146">NOTES</span></span>

## <span data-ttu-id="616cd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="616cd-147">RELATED LINKS</span></span>

[<span data-ttu-id="616cd-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="616cd-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


