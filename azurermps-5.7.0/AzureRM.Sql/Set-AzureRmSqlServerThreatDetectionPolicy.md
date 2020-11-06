---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 40ce06b21be7312598978bbd56b10e4e33915ece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526538"
---
# <span data-ttu-id="05db5-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="05db5-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="05db5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05db5-102">SYNOPSIS</span></span>
<span data-ttu-id="05db5-103">Ustawia zasady wykrywania zagrożeń na serwerze.</span><span class="sxs-lookup"><span data-stu-id="05db5-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05db5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05db5-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05db5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05db5-105">DESCRIPTION</span></span>
<span data-ttu-id="05db5-106">Polecenie cmdlet **Set-AzureRmSqlServerThreatDetectionPolicy** ustawia zasady wykrywania zagrożeń na platformie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05db5-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="05db5-107">W celu włączenia wykrywania zagrożeń na serwerze należy włączyć zasady inspekcji na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="05db5-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="05db5-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz nazwa_serwera identyfikujące serwer.</span><span class="sxs-lookup"><span data-stu-id="05db5-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="05db5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05db5-109">EXAMPLES</span></span>

### <span data-ttu-id="05db5-110">Przykład 1: Ustawianie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="05db5-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="05db5-111">To polecenie ustawia zasady wykrywania zagrożeń dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="05db5-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="05db5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05db5-112">PARAMETERS</span></span>

### <span data-ttu-id="05db5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05db5-113">-DefaultProfile</span></span>
<span data-ttu-id="05db5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="05db5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05db5-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="05db5-115">-EmailAdmins</span></span>
<span data-ttu-id="05db5-116">Określa, czy zasady wykrywania zagrożeń kontaktują się z administratorami za pomocą poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="05db5-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="05db5-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="05db5-118">Określa tablicę typów wykrywania, które należy wykluczyć z zasad.</span><span class="sxs-lookup"><span data-stu-id="05db5-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="05db5-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="05db5-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05db5-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="05db5-120">Sql_Injection</span></span>
- <span data-ttu-id="05db5-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="05db5-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="05db5-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="05db5-122">Access_Anomaly</span></span>
- <span data-ttu-id="05db5-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="05db5-123">None</span></span>

```yaml
Type: DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="05db5-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="05db5-125">Określa rozdzielaną średnikami listę adresów e-mail, do których zasady wysyłają powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="05db5-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05db5-126">-PassThru</span></span>
<span data-ttu-id="05db5-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="05db5-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="05db5-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="05db5-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="05db5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05db5-129">-ResourceGroupName</span></span>
<span data-ttu-id="05db5-130">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="05db5-130">Specifies the name of the resource group to which the server belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="05db5-131">-RetentionInDays</span></span>
<span data-ttu-id="05db5-132">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="05db5-132">The number of retention days for the audit logs</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="05db5-133">-ServerName</span></span>
<span data-ttu-id="05db5-134">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="05db5-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="05db5-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05db5-135">-StorageAccountName</span></span>
<span data-ttu-id="05db5-136">Określa nazwę konta magazynu, które ma być używane.</span><span class="sxs-lookup"><span data-stu-id="05db5-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="05db5-137">Używanie symboli wieloznacznych jest niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="05db5-137">Wildcards are not permitted.</span></span> <span data-ttu-id="05db5-138">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="05db5-138">This parameter is not required.</span></span> <span data-ttu-id="05db5-139">Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zasad wykrywania zagrożeń w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="05db5-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="05db5-140">Jeśli zasada wykrywania tagu THEAD Database jest po raz pierwszy zdefiniowana, a ten parametr nie zostanie podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="05db5-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05db5-141">-Confirm</span></span>
<span data-ttu-id="05db5-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05db5-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05db5-143">-WhatIf</span></span>
<span data-ttu-id="05db5-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05db5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05db5-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05db5-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05db5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05db5-146">CommonParameters</span></span>
<span data-ttu-id="05db5-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05db5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05db5-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05db5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05db5-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05db5-149">INPUTS</span></span>

###  
<span data-ttu-id="05db5-150">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05db5-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="05db5-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05db5-151">OUTPUTS</span></span>

### <span data-ttu-id="05db5-152">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="05db5-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="05db5-153">To polecenie cmdlet zwraca obiekt **ServerThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="05db5-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="05db5-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05db5-154">NOTES</span></span>

## <span data-ttu-id="05db5-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05db5-155">RELATED LINKS</span></span>

[<span data-ttu-id="05db5-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="05db5-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="05db5-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="05db5-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="05db5-158">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="05db5-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
