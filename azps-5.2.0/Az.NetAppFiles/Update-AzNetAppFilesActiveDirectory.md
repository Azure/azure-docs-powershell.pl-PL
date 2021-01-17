---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335317"
---
# <span data-ttu-id="adb8f-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="adb8f-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="adb8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="adb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="adb8f-103">Umożliwia zaktualizowanie konfiguracji usługi Active Directory dla usługi Azure NetApp (ANF) do określonych opcjonalnych modyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="adb8f-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="adb8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="adb8f-104">SYNTAX</span></span>

### <span data-ttu-id="adb8f-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="adb8f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb8f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adb8f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb8f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adb8f-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adb8f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="adb8f-108">DESCRIPTION</span></span>
<span data-ttu-id="adb8f-109">Polecenie cmdlet **Update-AzNetAppFilesAccount** modyfikuje konfigurację usługi ANF Active Directory.</span><span class="sxs-lookup"><span data-stu-id="adb8f-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="adb8f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="adb8f-110">EXAMPLES</span></span>

### <span data-ttu-id="adb8f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="adb8f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="adb8f-112">To polecenie wykonuje aktualizację dla danej konfiguracji usługi Active Directory, modyfikując tę nazwę użytkownika.</span><span class="sxs-lookup"><span data-stu-id="adb8f-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="adb8f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="adb8f-113">PARAMETERS</span></span>

### <span data-ttu-id="adb8f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="adb8f-114">-AccountName</span></span>
<span data-ttu-id="adb8f-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="adb8f-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="adb8f-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="adb8f-116">-AccountObject</span></span>
<span data-ttu-id="adb8f-117">Konto obiektu usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="adb8f-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="adb8f-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="adb8f-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="adb8f-119">Identyfikator usługi ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="adb8f-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb8f-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="adb8f-120">-AdName</span></span>
<span data-ttu-id="adb8f-121">Nazwa komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="adb8f-121">Name of the active directory machine.</span></span>
<span data-ttu-id="adb8f-122">Ten parametr opcjonalny jest wykorzystywany tylko podczas tworzenia woluminu Kerberos.</span><span class="sxs-lookup"><span data-stu-id="adb8f-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="adb8f-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="adb8f-123">-BackupOperator</span></span>
<span data-ttu-id="adb8f-124">Użytkownicy, którzy zostaną dodani do wbudowanej grupy usługi Active Directory operatora kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="adb8f-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="adb8f-125">Lista unikatowych nazw użytkowników bez specyfikatora domeny</span><span class="sxs-lookup"><span data-stu-id="adb8f-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="adb8f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb8f-126">-DefaultProfile</span></span>
<span data-ttu-id="adb8f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="adb8f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb8f-128">-DNS</span><span class="sxs-lookup"><span data-stu-id="adb8f-128">-Dns</span></span>
<span data-ttu-id="adb8f-129">Rozdzielana przecinkami lista adresów IP serwera DNS (tylko IPv4) domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="adb8f-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="adb8f-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="adb8f-130">-Domain</span></span>
<span data-ttu-id="adb8f-131">Nazwa domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="adb8f-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="adb8f-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="adb8f-132">-InputObject</span></span>
<span data-ttu-id="adb8f-133">Obiekt usługi Active Directory do usunięcia</span><span class="sxs-lookup"><span data-stu-id="adb8f-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adb8f-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="adb8f-134">-KdcIP</span></span>
<span data-ttu-id="adb8f-135">adresy IP serwera centrum dystrybucji kluczy dla komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="adb8f-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="adb8f-136">Ten parametr opcjonalny jest wykorzystywany tylko podczas tworzenia woluminu Kerberos.</span><span class="sxs-lookup"><span data-stu-id="adb8f-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="adb8f-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="adb8f-137">-OrganizationalUnit</span></span>
<span data-ttu-id="adb8f-138">Jednostka organizacyjna (OU) w usłudze Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="adb8f-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="adb8f-139">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="adb8f-139">-Password</span></span>
<span data-ttu-id="adb8f-140">Hasło zwykłego tekstu administratora domeny usługi Active Directory wartość jest zamaskowane w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="adb8f-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="adb8f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb8f-141">-ResourceGroupName</span></span>
<span data-ttu-id="adb8f-142">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="adb8f-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="adb8f-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="adb8f-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="adb8f-144">Gdy protokół LDAP przez protokół SSL/TLS jest włączony, klient LDAP musi mieć certyfikat certyfikatu głównego urzędu certyfikacji kodowany algorytmem Base64, ten parametr opcjonalny jest stosowany tylko dla dwóch protokołów z woluminami mapowania użytkowników LDAP.</span><span class="sxs-lookup"><span data-stu-id="adb8f-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="adb8f-145">-Site</span><span class="sxs-lookup"><span data-stu-id="adb8f-145">-Site</span></span>
<span data-ttu-id="adb8f-146">Witryna usługi Active Directory, do której usługa ma ograniczyć odnajdowanie kontrolera domeny</span><span class="sxs-lookup"><span data-stu-id="adb8f-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="adb8f-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="adb8f-147">-SmbServerName</span></span>
<span data-ttu-id="adb8f-148">Nazwa NetBIOS serwera SMB.</span><span class="sxs-lookup"><span data-stu-id="adb8f-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="adb8f-149">Ta nazwa będzie rejestrowana jako konto komputera w usłudze AD i używana do instalowania woluminów</span><span class="sxs-lookup"><span data-stu-id="adb8f-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="adb8f-150">-Username</span><span class="sxs-lookup"><span data-stu-id="adb8f-150">-Username</span></span>
<span data-ttu-id="adb8f-151">Nazwa użytkownika administratora domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="adb8f-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="adb8f-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adb8f-152">-Confirm</span></span>
<span data-ttu-id="adb8f-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb8f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb8f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb8f-154">-WhatIf</span></span>
<span data-ttu-id="adb8f-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb8f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb8f-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="adb8f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb8f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb8f-157">CommonParameters</span></span>
<span data-ttu-id="adb8f-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb8f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb8f-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adb8f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb8f-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adb8f-160">INPUTS</span></span>

### <span data-ttu-id="adb8f-161">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="adb8f-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="adb8f-162">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="adb8f-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="adb8f-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="adb8f-163">OUTPUTS</span></span>

### <span data-ttu-id="adb8f-164">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="adb8f-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="adb8f-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="adb8f-165">NOTES</span></span>

## <span data-ttu-id="adb8f-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adb8f-166">RELATED LINKS</span></span>
