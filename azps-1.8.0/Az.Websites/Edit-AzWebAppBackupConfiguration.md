---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4319a2637b2dbb008056a6b369ace539b889cd37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707346"
---
# <span data-ttu-id="c0fef-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fef-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="c0fef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0fef-102">SYNOPSIS</span></span>

## <span data-ttu-id="c0fef-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0fef-103">SYNTAX</span></span>

### <span data-ttu-id="c0fef-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c0fef-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="c0fef-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c0fef-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="c0fef-106">Opis</span><span class="sxs-lookup"><span data-stu-id="c0fef-106">DESCRIPTION</span></span>
<span data-ttu-id="c0fef-107">Polecenie cmdlet **Edit-AzWebAppBackupConfiguration** umożliwia edytowanie bieżącej kopii zapasowej konfiguracji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c0fef-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="c0fef-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0fef-108">EXAMPLES</span></span>

## <span data-ttu-id="c0fef-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0fef-109">PARAMETERS</span></span>

### <span data-ttu-id="c0fef-110">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="c0fef-110">-Databases</span></span>
<span data-ttu-id="c0fef-111">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c0fef-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="c0fef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fef-112">-DefaultProfile</span></span>
<span data-ttu-id="c0fef-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0fef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0fef-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="c0fef-114">-FrequencyInterval</span></span>
<span data-ttu-id="c0fef-115">Interwał częstotliwości</span><span class="sxs-lookup"><span data-stu-id="c0fef-115">Frequency Interval</span></span>

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

### <span data-ttu-id="c0fef-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="c0fef-116">-FrequencyUnit</span></span>
<span data-ttu-id="c0fef-117">Jednostka częstotliwości</span><span class="sxs-lookup"><span data-stu-id="c0fef-117">Frequency Unit</span></span>

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

### <span data-ttu-id="c0fef-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="c0fef-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="c0fef-119">Zachowywanie co najmniej jednej opcji kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="c0fef-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="c0fef-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0fef-120">-Name</span></span>
<span data-ttu-id="c0fef-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c0fef-121">WebApp Name</span></span>

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

### <span data-ttu-id="c0fef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0fef-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0fef-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c0fef-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c0fef-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c0fef-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="c0fef-125">Okres przechowywania w dniach</span><span class="sxs-lookup"><span data-stu-id="c0fef-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="c0fef-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="c0fef-126">-Slot</span></span>
<span data-ttu-id="c0fef-127">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="c0fef-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c0fef-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c0fef-128">-StartTime</span></span>
<span data-ttu-id="c0fef-129">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="c0fef-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="c0fef-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c0fef-130">-StorageAccountUrl</span></span>
<span data-ttu-id="c0fef-131">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c0fef-131">Storage Account Url</span></span>

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

### <span data-ttu-id="c0fef-132">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c0fef-132">-WebApp</span></span>
<span data-ttu-id="c0fef-133">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="c0fef-133">WebApp Object</span></span>

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

### <span data-ttu-id="c0fef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fef-134">CommonParameters</span></span>
<span data-ttu-id="c0fef-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0fef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fef-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0fef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fef-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0fef-137">INPUTS</span></span>

### <span data-ttu-id="c0fef-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c0fef-138">System.Int32</span></span>

### <span data-ttu-id="c0fef-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0fef-139">System.String</span></span>

### <span data-ttu-id="c0fef-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c0fef-140">System.DateTime</span></span>

### <span data-ttu-id="c0fef-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0fef-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c0fef-142">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="c0fef-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="c0fef-143">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c0fef-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="c0fef-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0fef-144">OUTPUTS</span></span>

### <span data-ttu-id="c0fef-145">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fef-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="c0fef-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0fef-146">NOTES</span></span>

## <span data-ttu-id="c0fef-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0fef-147">RELATED LINKS</span></span>

[<span data-ttu-id="c0fef-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0fef-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


