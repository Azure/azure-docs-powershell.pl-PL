---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489990"
---
# <span data-ttu-id="f386d-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="f386d-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="f386d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f386d-102">SYNOPSIS</span></span>
<span data-ttu-id="f386d-103">Tworzy nową konfigurację usługi Active Directory NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="f386d-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="f386d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f386d-104">SYNTAX</span></span>

### <span data-ttu-id="f386d-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f386d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f386d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f386d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f386d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f386d-107">DESCRIPTION</span></span>
<span data-ttu-id="f386d-108">Polecenie cmdlet **New-AzNetAppFilesActiveDirectory** tworzy nową konfigurację usługi Active Directory dla konta usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="f386d-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="f386d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f386d-109">EXAMPLES</span></span>

### <span data-ttu-id="f386d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f386d-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="f386d-111">To polecenie pobiera hasło usługi AD z Promt do secreates w nowej konfiguracji usługi Active Directory dla konta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="f386d-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="f386d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f386d-112">PARAMETERS</span></span>

### <span data-ttu-id="f386d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f386d-113">-AccountName</span></span>
<span data-ttu-id="f386d-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="f386d-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="f386d-115">-AccountObject</span></span>
<span data-ttu-id="f386d-116">Konto nowego obiektu zasad kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f386d-116">The Account for the new Backup Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="f386d-117">-AdName</span></span>
<span data-ttu-id="f386d-118">Nazwa komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f386d-118">Name of the active directory machine.</span></span>
<span data-ttu-id="f386d-119">Ten parametr opcjonalny jest wykorzystywany tylko podczas tworzenia woluminu Kerberos.</span><span class="sxs-lookup"><span data-stu-id="f386d-119">This optional parameter is used only while creating kerberos volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="f386d-120">-BackupOperator</span></span>
<span data-ttu-id="f386d-121">Użytkownicy, którzy zostaną dodani do wbudowanej grupy usługi Active Directory operatora kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f386d-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="f386d-122">Lista unikatowych nazw użytkowników bez specyfikatora domeny</span><span class="sxs-lookup"><span data-stu-id="f386d-122">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f386d-123">-DefaultProfile</span></span>
<span data-ttu-id="f386d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f386d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f386d-125">-DNS</span><span class="sxs-lookup"><span data-stu-id="f386d-125">-Dns</span></span>
<span data-ttu-id="f386d-126">Rozdzielana przecinkami lista adresów IP serwera DNS (tylko IPv4) domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="f386d-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="f386d-127">-Domain</span></span>
<span data-ttu-id="f386d-128">Nazwa domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="f386d-128">Name of the Active Directory domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="f386d-129">-KdcIP</span></span>
<span data-ttu-id="f386d-130">adresy IP serwera centrum dystrybucji kluczy dla komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f386d-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="f386d-131">Ten parametr opcjonalny jest wykorzystywany tylko podczas tworzenia woluminu Kerberos.</span><span class="sxs-lookup"><span data-stu-id="f386d-131">This optional parameter is used only while creating kerberos volume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="f386d-132">-OrganizationalUnit</span></span>
<span data-ttu-id="f386d-133">Jednostka organizacyjna (OU) w usłudze Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="f386d-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-134">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="f386d-134">-Password</span></span>
<span data-ttu-id="f386d-135">Hasło zwykłego tekstu administratora domeny usługi Active Directory wartość jest zamaskowane w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="f386d-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f386d-136">-ResourceGroupName</span></span>
<span data-ttu-id="f386d-137">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="f386d-137">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="f386d-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="f386d-139">Gdy protokół LDAP przez protokół SSL/TLS jest włączony, klient LDAP musi mieć certyfikat certyfikatu głównego urzędu certyfikacji kodowany algorytmem Base64, ten parametr opcjonalny jest stosowany tylko dla dwóch protokołów z woluminami mapowania użytkowników LDAP.</span><span class="sxs-lookup"><span data-stu-id="f386d-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-140">-Site</span><span class="sxs-lookup"><span data-stu-id="f386d-140">-Site</span></span>
<span data-ttu-id="f386d-141">Witryna usługi Active Directory, do której usługa ma ograniczyć odnajdowanie kontrolera domeny</span><span class="sxs-lookup"><span data-stu-id="f386d-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="f386d-142">-SmbServerName</span></span>
<span data-ttu-id="f386d-143">Nazwa NetBIOS serwera SMB.</span><span class="sxs-lookup"><span data-stu-id="f386d-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="f386d-144">Ta nazwa będzie rejestrowana jako konto komputera w usłudze AD i używana do instalowania woluminów</span><span class="sxs-lookup"><span data-stu-id="f386d-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-145">-Username</span><span class="sxs-lookup"><span data-stu-id="f386d-145">-Username</span></span>
<span data-ttu-id="f386d-146">Nazwa użytkownika administratora domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="f386d-146">Username of Active Directory domain administrator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f386d-147">-Confirm</span></span>
<span data-ttu-id="f386d-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f386d-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f386d-149">-WhatIf</span></span>
<span data-ttu-id="f386d-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f386d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f386d-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f386d-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f386d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f386d-152">CommonParameters</span></span>
<span data-ttu-id="f386d-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f386d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f386d-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f386d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f386d-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f386d-155">INPUTS</span></span>

### <span data-ttu-id="f386d-156">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f386d-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f386d-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f386d-157">OUTPUTS</span></span>

### <span data-ttu-id="f386d-158">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="f386d-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="f386d-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f386d-159">NOTES</span></span>

## <span data-ttu-id="f386d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f386d-160">RELATED LINKS</span></span>
